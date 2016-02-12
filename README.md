# datatables-links
add links to table rows
when you click a row it redirects to the given url



# install (laravel)
    <script src="{{ asset('/plugins/datatables-links/jquery.datatables.links.js') }}"></script>

or normal

    <script src="datatables-links/jquery.datatables.links.js"></script>


# usage

    dTObject = "products"; //The dataTable id
    dTObjectUrl = "{{ url('/admin/products/info/') }}/"; // The first part of the url 
    dTObjectUrl2 = "/delete"; // The second part of the url
    // eg. url 1 >/admin/products/info/< {productid} url 2 >/delete<
    dTObjectNot = ":first-child,.remove,.edit"; // Exclude columns with those classes
    
    $("#"+dTObject).DataTable(); // Init the DataTable plugin
    
    $("#"+dTObject).datatablesLinks(dTObject, dTObjectUrl, dTObjectUrl2, dTObjectNot, false); // Init the DataTable-Links plugin
    
    // The 5th option {false, true} toggles the option to select rows by clicking on the ID column
    
