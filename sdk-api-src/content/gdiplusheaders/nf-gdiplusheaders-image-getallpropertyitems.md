---
UID: NF:gdiplusheaders.Image.GetAllPropertyItems
title: Image::GetAllPropertyItems
author: windows-sdk-content
description: The Image::GetAllPropertyItems method gets all the property items (metadata) stored in this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getallpropertyitems.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetAllPropertyItems, GetAllPropertyItems method [GDI+], GetAllPropertyItems method [GDI+],Image class, Image class [GDI+],GetAllPropertyItems method, Image.GetAllPropertyItems, Image::GetAllPropertyItems, _gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_, gdiplus._gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetAllPropertyItems
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::GetAllPropertyItems


## -description


The <b>Image::GetAllPropertyItems</b> method gets all the property items (metadata) stored in this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param totalBufferSize [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the 
					<i>allItems</i> buffer. Call the <a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a> method to obtain the required size. 


### -param numProperties [in]

Type: <b>UINT</b>

Integer that specifies the number of properties in the image. Call the <a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a> method to obtain this number. 


### -param allItems [out]

Type: <b><a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a> objects that receives the property items. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.




## -remarks



Some image files contain metadata that you can read to determine features of the image. For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.

GDI+ stores an individual piece of metadata in a <a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a> object. The <b>Image::GetAllPropertyItems</b> method returns an array of <b>PropertyItem</b> objects. Before you call <b>Image::GetAllPropertyItems</b>, you must allocate a buffer large enough to receive that array. You can call the <a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a> method of an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object to get the size, in bytes, of the required buffer. The <b>Image::GetPropertySize</b> method also gives you the number of properties (pieces of metadata) in the image.

Several enumerations and constants related to image metadata are defined in Gdiplusimaging.h.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a JPEG file. The code calls the <b>GetAllPropertyItems</b> method of that 
						<b>Image</b> object to obtain its property items (metadata).

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

   // Find out how many property items are in the image, and find out the
   // required size of the buffer that will receive those property items.
   UINT totalBufferSize;
   UINT numProperties;
   image-&gt;GetPropertySize(&amp;totalBufferSize, &amp;numProperties);

   // Allocate the buffer that will receive the property items.
   PropertyItem* pAllItems = (PropertyItem*)malloc(totalBufferSize);

   // Fill the buffer.
   image-&gt;GetAllPropertyItems(totalBufferSize, numProperties, pAllItems);

// Print the id data member of each property item.
   for(UINT j = 0; j &lt; numProperties; ++j)
   {
      printf("%x\n", pAllItems[j].id);
   }

   free(pAllItems);
   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>320
10f
110
9003
829a
5090
5091</pre>
</td>
</tr>
</table></span></div>
The preceding output shows a hexadecimal ID number for each property item. You can look up those ID numbers in Gdiplusimaging.h and find out that they represent the following property tags.

<table class="clsStd">
<tr>
<th>Hexadecimal value</th>
<th>Property tag</th>
</tr>
<tr>
<td>0x0320</td>
<td>PropertyTagImageTitle</td>
</tr>
<tr>
<td>0x010f</td>
<td>PropertyTagEquipMake</td>
</tr>
<tr>
<td>0x0110</td>
<td>PropertyTagEquipModel</td>
</tr>
<tr>
<td>0x9003</td>
<td>PropertyTagExifDTOriginal</td>
</tr>
<tr>
<td>0x829a</td>
<td>PropertyTagExifExposureTime</td>
</tr>
<tr>
<td>0x5090</td>
<td>PropertyTagLuminanceTable</td>
</tr>
<tr>
<td>0x5091</td>
<td>PropertyTagChrominanceTable</td>
</tr>
</table>
 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fff3acf1-2a2f-46b6-af7e-02b7ef52bb40">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/2318eb42-9006-4361-ac5c-4e5325dc4947">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/ca96c4a3-058f-4ba4-a8be-2692ecd76710">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/574d3d5b-2440-4ab4-9d90-75282ea0f10d">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/ad849843-80e7-4773-96b0-f50dbdbfd61b">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/20201f1e-fa80-4a7b-b7cc-7737d4a434a5">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/449f8ba0-0c94-4733-80e1-1c03819e4c39">PropertyItem</a>



<a href="https://msdn.microsoft.com/2febea35-3fea-4a2d-baaf-7a4f935fc81f">Reading and Writing Metadata</a>
 

 

