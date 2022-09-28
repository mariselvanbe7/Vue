<template>
    <li>
        <h2>{{name}}</h2>
        <button @click="toggleDetails">Show details</button>
        <ul v-if="detailsAreVisible">
            <li><strong>Phone :</strong>{{phoneNumber}}</li>
            <li><strong>Email :</strong>{{emailAddress}}</li>
        </ul>
    </li>
    
</template>

<script>
export default{
   props :[
    'name',
    'phoneNumber',
    'emailAddress'
   ],
    data(){
        return {
            detailsAreVisible : false,
            friends :{
                
          Id: 'loose1',
          name: 'dfhdfhfhdfudsuif',
          phone: '7653475348',
          email: 'loose1@gamill.com'

        
            },
        };
    },
    methods: {
        toggleDetails() {
            this.detailsAreVisible = !this.detailsAreVisible;
        }
    }
}

</script>
