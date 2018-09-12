---
UID: NF:gdiplusheaders.Image.GetPropertyItem
title: Image::GetPropertyItem
author: windows-sdk-content
description: The Image::GetPropertyItem method gets a specified property item (piece of metadata) from this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpropertyitem.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetPropertyItem, GetPropertyItem method [GDI+], GetPropertyItem method [GDI+],Image class, Image class [GDI+],GetPropertyItem method, Image.GetPropertyItem, Image::GetPropertyItem, _gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_, gdiplus._gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_
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
 - Image.GetPropertyItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetPropertyItem


## -description


The <b>Image::GetPropertyItem</b> method gets a specified property item (piece of metadata) from this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.


## -parameters




### -param propId [in]

Type: <b>PROPID</b>

Integer that identifies the property item to be retrieved. 


### -param propSize [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the property item to be retrieved. Call the <a href="https://msdn.microsoft.com/en-us/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a> method to determine the size. 


### -param buffer [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a> object that receives the property item. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



The <b>Image::GetPropertyItem</b> method returns a <a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a> object. Before you call 
				<b>Image::GetPropertyItem</b>, you must allocate a buffer large enough to receive that object — the size varies according to data type and value of the property item. You can call the <a href="https://msdn.microsoft.com/en-us/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a> method of an 
				<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object to get the size, in bytes, of the required buffer.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object based on a JPEG file. The code gets the make of the camera that captured the image by passing the PropertyTagEquipMake constant to the <b>Image::GetPropertyItem</b> method of the 
						<b>Image</b> object.

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

   UINT size = 0;
   PropertyItem* propertyItem = NULL;
   Image* image = new Image(L"FakePhoto.jpg");

   // Assume that the image has a property item of type PropertyItemEquipMake.
   // Get the size of that property item.
   size = image-&gt;GetPropertyItemSize(PropertyTagEquipMake);

   // Allocate a buffer to receive the property item.
   propertyItem = (PropertyItem*)malloc(size);

   // Get the property item.
   image-&gt;GetPropertyItem(PropertyTagEquipMake, size, propertyItem);

   // Display the members of the retrieved PropertyItem object.
   printf("The length of the property item is %u.\n", propertyItem-&gt;length);
   printf("The data type of the property item is %u.\n", propertyItem-&gt;type);

   if(propertyItem-&gt;type == PropertyTagTypeASCII)
      printf("The value of the property item is %s.\n", propertyItem-&gt;value);

   free(propertyItem);
   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, FakePhoto.jpg, produced the following output. Note that the data type is 2, the value of the PropertyTagTypeASCII constant that is defined in Gdiplusimaging.h.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>The length of the property item is 17.
The data type of the property item is 2.
The value of the property item is Northwind Traders.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535372(v=VS.85).aspx">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535388(v=VS.85).aspx">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535389(v=VS.85).aspx">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535392(v=VS.85).aspx">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535400(v=VS.85).aspx">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535405(v=VS.85).aspx">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533832(v=VS.85).aspx">Reading and Writing Metadata</a>
 

 

