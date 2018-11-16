---
UID: NF:gdiplusheaders.Image.RemovePropertyItem
title: Image::RemovePropertyItem
author: windows-sdk-content
description: The Image::RemovePropertyItem method removes a property item (piece of metadata) from this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_RemovePropertyItem_propId_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\removepropertyitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Image class [GDI+],RemovePropertyItem method, Image.RemovePropertyItem, Image::RemovePropertyItem, RemovePropertyItem, RemovePropertyItem method [GDI+], RemovePropertyItem method [GDI+],Image class, _gdiplus_CLASS_Image_RemovePropertyItem_propId_, gdiplus._gdiplus_CLASS_Image_RemovePropertyItem_propId_
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
 - Image.RemovePropertyItem
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
- Image.RemovePropertyItem
: 
req.product: GDI+ 1.0
---

# Image::RemovePropertyItem


## -description


The <b>Image::RemovePropertyItem</b> method removes a property item (piece of metadata) from this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param propId [in]

Type: <b>PROPID</b>

Integer that identifies the property item to be removed. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The <b>Image::RemovePropertyItem</b> method removes a specified property from an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object, but that property item is not removed from the file or stream that was used to construct the 
				<b>Image</b> object. To save the image (with the property item removed) to a new JPEG file or stream, call the 
				<b>Save</b> method of the 
				<b>Image</b> object.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a JPEG file. The code removes the PropertyTagEquipMake property item from the 
						<b>Image</b> object by calling its <b>Image::RemovePropertyItem</b> method. The code calls <a href="https://msdn.microsoft.com/574d3d5b-2440-4ab4-9d90-75282ea0f10d">Image::GetPropertyItemSize</a> twice (once before and once after removing the item) to determine the size of the PropertyTagEquipMake property item. The code does not remove the property item from the image file; it removes the property item only from the 
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

   Image* image = new Image(L"FakePhoto3.jpg");
   UINT size = 0;

   size = image-&gt;GetPropertyItemSize(PropertyTagEquipMake);
   printf("The size of the PropertyTagEquipMake item is %u.\n", size);

   image-&gt;RemovePropertyItem(PropertyTagEquipMake);   

   size = image-&gt;GetPropertyItemSize(PropertyTagEquipMake);
   printf("The size of the PropertyTagEquipMake item is %u.\n", size);

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, FakePhoto3.jpg, produced the following output:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>The size of the PropertyTagEquipMake item is 33.
The size of the PropertyTagEquipMake item is 0.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/c22c2027-9552-4f35-ba44-755d872ceea7">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/fff3acf1-2a2f-46b6-af7e-02b7ef52bb40">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/2318eb42-9006-4361-ac5c-4e5325dc4947">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/ca96c4a3-058f-4ba4-a8be-2692ecd76710">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/574d3d5b-2440-4ab4-9d90-75282ea0f10d">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/20201f1e-fa80-4a7b-b7cc-7737d4a434a5">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a>



<a href="https://msdn.microsoft.com/2febea35-3fea-4a2d-baaf-7a4f935fc81f">Reading and Writing Metadata</a>
 

 

