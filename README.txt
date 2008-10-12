== File Type Icons

File icons you can use for attachments with Paperclip or Attachment Fu or... anything. I didn't create them, just converted them to pngs, resized them and added a couple common file types (.ai, .psd, .rb (of course)).

The original files can be found here:
http://www.iconiza.com/downloads/index.php

== License Information

The license is Creative Commons Attribution-ShareAlike 2.5. You can attribute the original creator:

Michael Müller C. 
Web Designer and Developer

E-mail: mmuller@mmcdesign.com 
E-mail: mullercardenas@gmail.com
Website: www.mmcdesign.com 
Blog: blog.mmcdesign.com


== Use in Ruby on Rails
In Rails I put the following in a helper:

def icon_for(filename, options={})
  ext = filename.match(/[.](\w{1,6})\Z/)[1]
  size = "#{options[:size]}/" if options[:size]
  "/file_icons/#{size ||=""}#{ext}.png"
end

Pass it a filename and it returns the path to the proper icon. It does not check to make sure the icon exists.