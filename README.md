View More & less
------------------------------------------------------------

 <p *ngIf="!is_view_more" class=" mb-0 d-lg-none">{{ (serviceDescription?.length>50)? (serviceDescription |
              slice:0:50)+'..':(serviceDescription) }}</p>
            <p *ngIf="is_view_more" class=" mb-0">{{serviceDescription}}</p>
            <a *ngIf="serviceDescription?.length>50 && !is_view_less" href="javascript:void(0)"
              class="text-theme-vd d-lg-none" (click)="viewMore()">{{'viewMore'|translate}}</a>
            <a *ngIf="is_view_less" href="javascript:void(0)" class="text-theme-vd d-lg-none" (click)="viewLess()">{{'viewLess'|translate}}
              </a>
			  
		
		TS Code
		---------------------------------------
		
		  serviceDescription: any;
		    is_view_more: boolean = false;
			is_view_less: boolean = false;
			
viewMore() {
    this.is_view_more = true;
    this.is_view_less = true;
  }
  viewLess() {
    this.is_view_more = false;
    this.is_view_less = false;
  }
