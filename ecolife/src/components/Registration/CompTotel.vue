<template> 
  <div class="w-75pr_lg-90pr_md-100pr row justify-center"> 
    <div class=" w-90pr br-6px shadow-up"> 
      <div v-for="son in sons" :key="son" class=" w-100pr q-pt-sm"> 
        <div class="q-ml-sm q-mr-sm text-subtitle2">{{son.sonlar}} items</div> 
        <q-list class="rounded-borders" /> 
        <q-expansion-item expand-separator label="show details"> 
          <q-card  > 
            <q-card-section v-for="item in items" :key="item"> 
              <div>{{item.shops}}</div> 
              <div>{{item.shop}}</div> 
 
              <div class="row justify-between"> 
                <div>{{item.angel}}</div> 
                <div style="color: blueviolet">{{item.size}}</div> 
              </div> 

            </q-card-section> 
          </q-card> 
        </q-expansion-item> 
        <div v-for="main in mains" :key="main">
            <div class="row justify-between text-subtitle2 q-ml-sm q-mr-sm"> 
              <div>Subtotal</div> 
              <div>{{main.Subtotal}}</div> 
            </div> 
            <div class="row justify-between text-subtitle2 q-ml-sm q-mr-sm"> 
              <div>Shipping</div> 
              <div>{{main.Shipping}}</div> 
            </div> 
            </div>
            <br /> 
      </div> 
      <div v-for="dont in donts" :key="dont">
          <div class="row justify-between text-subtitle2 q-ml-sm q-mr-sm"> 
            <div>Total (Tax Excl.)</div> 
            <div>{{dont.total}}</div> 
          </div> 
          <div class="row justify-between text-subtitle2 q-ml-sm q-mr-sm"> 
            <div>Taxes</div> 
            <div>{{dont.text}}</div> 
          </div> 
      </div>
      <br /> 

      
    </div><br> 
 
    <div class="w-90pr colum justify-center mt-25px pl-15px"> 
 
      <div class="row justify-center w-100pr"> 
        <q-icon class="text-h3" color="grey" name="delivery_dining"></q-icon> 
        <div class="w-80pr q-ml-md text-grey">Security Policy (Edit With Customer Reassurance Module)</div> 
      </div><br> 
 
      <div class="row justify-center w-100pr"> 
        <q-icon class="text-h3" color="grey" name="keyboard_return"></q-icon> 
        <div class="w-80pr q-ml-md text-grey">Delivery Policy (Edit With Customer Reassurance Module)</div> 
      </div><br> 
 
      <div class="row justify-center w-100pr"> 
        <q-icon class="text-h3 " color="grey" name="currency_exchange"></q-icon> 
        <div class="w-80pr q-ml-md text-grey">Return Policy (Edit With Customer Reassurance Module)</div> 
      </div> 
    </div> 
  </div> 
 
</template> 
 
<script> 
export default {
  data(){
    return{
      sons:[
        {sonlar:'2'}
      ],
      items:[
        {shops:'Originals Kaval Windbreaker Winte Jacket 2',
        shop:'x1',
        angel:'Size: S',
        size:'$21.51',
        }        
      ],
      mains:[
      { 
         Subtotal:'$33.41',
        Shipping:'$7.00'}
      ],
      donts:[
        {
          total:'$40.41',
          text:'$0.00'
        }
      ]
    }
  }
} 
</script> 
 
<style scoped> 
.shadow-up{
  box-shadow: 3px 3px 15px 0px rgb(186, 185, 185);
}
.btn { 
  border: none; 
} 
 
.contier { 
  border-bottom: 1px solid grey; 
} 
.w-75pr_lg-90pr_md-100pr{
  width: 75%;
}


@media screen and (max-width:1399px) {
  .w-75pr_lg-90pr_md-100pr{
  width: 100%;
}
}
</style>
    