---
UID: NF:gdiplusheaders.Image.SetPropertyItem
title: Image::SetPropertyItem
author: windows-sdk-content
description: The Image::SetPropertyItem method sets a property item (piece of metadata) for this Image object. If the item already exists, then its contents are updated; otherwise, a new item is added.
old-location: gdiplus\_gdiplus_CLASS_Image_SetPropertyItem_item_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setpropertyitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Image class [GDI+],SetPropertyItem method, Image.SetPropertyItem, Image::SetPropertyItem, SetPropertyItem, SetPropertyItem method [GDI+], SetPropertyItem method [GDI+],Image class, _gdiplus_CLASS_Image_SetPropertyItem_item_, gdiplus._gdiplus_CLASS_Image_SetPropertyItem_item_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.SetPropertyItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.SetPropertyItem
: 
req.product: GDI+ 1.0
---

# Image::SetPropertyItem


## -description


The <b>Image::SetPropertyItem</b> method sets a property item (piece of metadata) for this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. If the item already exists, then its contents are updated; otherwise, a new item is added.


## -parameters




### -param item [in]

Type: <b>const PropertyItem*</b>

Pointer to a <a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a> object that specifies the property item to be set. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Certain image formats (for example, ICON and EMF) don't support properties. If you call the <b>Image::SetPropertyItem</b> method on an image that doesn't support properties, it will return PropertyNotSupported.


#### Examples



The following console application creates a 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a JPEG file. The code calls the <b>Image::SetPropertyItem</b> method of that 
						<b>Image</b> object to set the title of the image. Then the code retrieves and displays the new title.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;gdiplus.h&gt;
#include &lt;stdio.h&gt;
using namespace Gdiplus;

INT main()
{
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&amp;gdiplusToken, &amp;gdiplusStartupInput, NULL);

   // Create an Image object based on a JPEG file.
   Image* image = new Image(L"FakePhoto.jpg");

   // Set the image title.
   PropertyItem* propItem = new PropertyItem;
   CHAR newTitleValue[] = "Fake Photograph 2";

   propItem-&gt;id = PropertyTagImageTitle;
   propItem-&gt;length = 18;  //  includes null terminator
   propItem-&gt;type = PropertyTagTypeASCII;
   propItem-&gt;value = newTitleValue;

   image-&gt;SetPropertyItem(propItem);

   // Get and display the new image title.
   UINT size = image-&gt;GetPropertyItemSize(PropertyTagImageTitle);
   PropertyItem* title = (PropertyItem*)malloc(size);
   image-&gt;GetPropertyItem(PropertyTagImageTitle, size, title);
   printf("The image title is %s.\n", title-&gt;value);

   free(title);
   delete propItem;
   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fff3acf1-2a2f-46b6-af7e-02b7ef52bb40">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/2318eb42-9006-4361-ac5c-4e5325dc4947">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/ca96c4a3-058f-4ba4-a8be-2692ecd76710">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/574d3d5b-2440-4ab4-9d90-75282ea0f10d">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/ad849843-80e7-4773-96b0-f50dbdbfd61b">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a>



<a href="https://msdn.microsoft.com/2febea35-3fea-4a2d-baaf-7a4f935fc81f">Reading and Writing Metadata</a>
 

 

