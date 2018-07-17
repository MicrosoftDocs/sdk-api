---
UID: NF:gdiplusheaders.Image.GetPropertySize
title: Image::GetPropertySize
author: windows-sdk-content
description: The Image::GetPropertySize method gets the total size, in bytes, of all the property items stored in this Image object. The Image::GetPropertySize method also gets the number of property items stored in this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpropertysize.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetPropertySize, GetPropertySize method [GDI+], GetPropertySize method [GDI+],Image class, Image class [GDI+],GetPropertySize method, Image.GetPropertySize, Image::GetPropertySize, _gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_, gdiplus._gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_
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
 - Image.GetPropertySize
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::GetPropertySize


## -description


The <b>Image::GetPropertySize</b> method gets the total size, in bytes, of all the property items stored in this 
			<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object. The <b>Image::GetPropertySize</b> method also gets the number of property items stored in this 
			<b>Image</b> object.


## -parameters




### -param totalBufferSize [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of all the property items. 


### -param numProperties [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the number of property items. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



Windows GDI+ stores an individual piece of metadata in a <a href="https://msdn.microsoft.com/library/ms534493(v=VS.85).aspx">PropertyItem</a> object. The <a href="https://msdn.microsoft.com/library/ms535372(v=VS.85).aspx">Image::GetAllPropertyItems</a> method returns an array of <b>PropertyItem</b> objects. Before you call <b>Image::GetAllPropertyItems</b>, you must allocate a buffer large enough to receive that array. You can call the <b>Image::GetPropertySize</b> method of an 
				<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object to get the size, in bytes, of the required buffer. The <b>Image::GetPropertySize</b> method also gives you the number of properties (pieces of metadata) in the image.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object based on a JPEG file. The code calls the <a href="https://msdn.microsoft.com/library/ms535372(v=VS.85).aspx">Image::GetAllPropertyItems</a> method of that 
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

   // Print the ID of each property item.
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
The preceding output shows the hexadecimal value of each property identifier. You can look up those numbers in Gdiplusimaging.h and find out that they represent the following property tags.


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




<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/library/ms535372(v=VS.85).aspx">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/library/ms535388(v=VS.85).aspx">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/library/ms535389(v=VS.85).aspx">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/library/ms535390(v=VS.85).aspx">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/library/ms535400(v=VS.85).aspx">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/library/ms535405(v=VS.85).aspx">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/library/ms534493(v=VS.85).aspx">PropertyItem</a>



<a href="https://msdn.microsoft.com/library/ms533832(v=VS.85).aspx">Reading and Writing Metadata</a>
 

 

