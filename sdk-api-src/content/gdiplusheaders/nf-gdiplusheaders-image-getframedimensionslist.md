---
UID: NF:gdiplusheaders.Image.GetFrameDimensionsList
title: Image::GetFrameDimensionsList
author: windows-sdk-content
description: The Image::GetFrameDimensionsList method gets the identifiers for the frame dimensions of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetFrameDimensionsList_dimensionIDs_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getframedimensionslist.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFrameDimensionsList, GetFrameDimensionsList method [GDI+], GetFrameDimensionsList method [GDI+],Image class, Image class [GDI+],GetFrameDimensionsList method, Image.GetFrameDimensionsList, Image::GetFrameDimensionsList, _gdiplus_CLASS_Image_GetFrameDimensionsList_dimensionIDs_count_, gdiplus._gdiplus_CLASS_Image_GetFrameDimensionsList_dimensionIDs_count_
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
 - Image.GetFrameDimensionsList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetFrameDimensionsList


## -description


The <b>Image::GetFrameDimensionsList</b> method gets the identifiers for the frame dimensions of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param dimensionIDs [out]

Type: <b>GUID*</b>

Pointer to an array that receives the identifiers. 
					GUIDs that identify various dimensions are defined in Gdiplusimaging.h. 


### -param count [in]

Type: <b>UINT</b>

Integer that specifies the number of elements in the 
					<i>dimensionIDs</i> array. Call the 
					<a href="https://msdn.microsoft.com/0d16501c-eedd-4cd4-85f3-f6c150b01af9">Image::GetFrameDimensionsCount</a> method to determine this number. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



This method returns information about multiple-frame images, which come in two styles: multiple page and multiple resolution. 

A multiple-page image is an image that contains more than one image. Each page contains a single image (or frame). These pages (or images, or frames) are typically displayed in succession to produce an animated sequence, such as in an animated GIF file. 

A multiple-resolution image is an image that contains more than one copy of an image at different resolutions.

Windows GDI+ can support an arbitrary number of pages (or images, or frames), as well as an arbitrary number of resolutions.


#### Examples



The following console application creates an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a TIFF file. The code calls the <a href="https://msdn.microsoft.com/0d16501c-eedd-4cd4-85f3-f6c150b01af9">Image::GetFrameDimensionsCount</a> method to find out how many frame dimensions the 
						<b>Image</b> object has. Each of those frame dimensions is identified by a 
						GUID, and the call to <b>GetFrameDimensionsList</b> retrieves those 
						GUIDs. The first 
						GUID is at index 0 in the 
						<i>pDimensionIDs</i> array. The call to the <a href="https://msdn.microsoft.com/11ea08ad-a425-4307-b86a-ab2532de4fff">Image::GetFrameCount</a> method determines the number of frames in the dimension identified by the first 
						GUID.

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

   Image* image = new Image(L"Multiframe.tif");

   // How many frame dimensions does the Image object have?
   UINT count = 0;
   count = image-&gt;GetFrameDimensionsCount();
   printf("The number of dimensions is %d.\n", count);
   GUID* pDimensionIDs = (GUID*)malloc(sizeof(GUID)*count);

   // Get the list of frame dimensions from the Image object.
   image-&gt;GetFrameDimensionsList(pDimensionIDs, count);

   // Display the GUID of the first (and only) frame dimension.
   WCHAR strGuid[39];
   StringFromGUID2(pDimensionIDs[0], strGuid, 39);
   wprintf(L"The first (and only) dimension ID is %s.\n", strGuid);

   // Get the number of frames in the first dimension.
   UINT frameCount = image-&gt;GetFrameCount(&amp;pDimensionIDs[0]);
   printf("The number of frames in that dimension is %d.\n", frameCount);
    
   free(pDimensionIDs);
   delete(image);
   GdiplusShutdown(gdiplusToken);
   return 0;
}</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, Multiframe.tif, produced the following output:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>The number of dimensions is 1.
The first (and only) dimension ID is {7462DC86-6180-4C7E-8E3F-EE7333A7A483}.
The number of frames in that dimension is 4.</pre>
</td>
</tr>
</table></span></div>
You can look up the displayed GUID in Gdiplusimaging.h and see that it is the identifier for the page dimension. So the program output tells us that the file Multiframe.tif has four pages; that is, four frames in the page dimension.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/dfed0b61-2230-4911-a642-0a6e4beb08d6">Copying Individual Frames from a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/9b61e01d-0a98-4ac3-865e-7570ed0c3cde">Creating and Saving a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/11ea08ad-a425-4307-b86a-ab2532de4fff">Image::GetFrameCount</a>



<a href="https://msdn.microsoft.com/0d16501c-eedd-4cd4-85f3-f6c150b01af9">Image::GetFrameDimensionsCount</a>



<a href="https://msdn.microsoft.com/e597f6e6-6e07-4afb-8905-26e4af961685">Image::SaveAdd Methods</a>
 

 

