# Paperclip with Hobo

Install this plugin alongside [paperclip](http://jimneath.org/2008/04/17/paperclip-attaching-files-in-rails/).

It adds two small things:

 - Automatically declares the fields for you, so you can just add
 
        has_attached_file :photo

   to your model, and then run the migration generator
   
 - Declares an input field
 
        <def tag="input" for="Paperclip::Attachment">
          <%= file_field_tag param_name_for_this, attributes %>
        </def>
        
    (to get this, you need `<include src="paperclip" plugin="paperclip_with_hobo">` in application.dryml)
