---
UID: NF:gdiplusheaders.Image.GetThumbnailImage
title: Image::GetThumbnailImage
author: windows-sdk-content
description: The Image::GetThumbnailImage method gets a thumbnail image from this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getthumbnailimage.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetThumbnailImage, GetThumbnailImage method [GDI+], GetThumbnailImage method [GDI+],Image class, Image class [GDI+],GetThumbnailImage method, Image.GetThumbnailImage, Image::GetThumbnailImage, _gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_, gdiplus._gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_
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
 - Image.GetThumbnailImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetThumbnailImage


## -description


The <b>Image::GetThumbnailImage</b> method gets a thumbnail image from this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param thumbWidth [in]

Type: <b>UINT</b>

Width, in pixels, of the requested thumbnail image. 


### -param thumbHeight [in]

Type: <b>UINT</b>

Height, in pixels, of the requested thumbnail image. 


### -param callback [in]

Type: <b>GetThumbnailImageAbort</b>

Optional. Callback function that you provide. During the process of creating or retrieving the thumbnail image, GDI+ calls this function to give you the opportunity to abort the process. The default value is <b>NULL</b>. 


### -param callbackData

Type: <b>VOID*</b>

Optional. Pointer to a block of memory that contains data to be used by the callback function. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>
</strong>

This method returns a pointer to an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that contains the thumbnail image.




## -remarks



A thumbnail image is a small copy of an image. Some image files have a thumbnail image embedded in the file. In such cases, this method retrieves the embedded thumbnail image. If there is no embedded thumbnail image, this method creates a thumbnail image by scaling the main image to the size specified in the 
				<i>thumbWidth</i> and 
				<i>thumbHeight</i> parameters. If both of those parameters are 0, a system-defined size is used.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a JPEG file. The code calls the <b>Image::GetThumbnailImage</b> method of that 
						<b>Image</b> object and then displays the thumbnail image along with the main image.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetThumbnail(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an image and a thumbnail of the image.
   Image image(L"Crayons.jpg");
   Image* pThumbnail = image.GetThumbnailImage(40, 40, NULL, NULL);

   // Draw the original and the thumbnail images.
   graphics.DrawImage(&amp;image, 10, 10, image.GetWidth(), image.GetHeight());
   graphics.DrawImage(
      pThumbnail, 
      150, 
      10, 
      pThumbnail-&gt;GetWidth(), 
      pThumbnail-&gt;GetHeight());

   delete pThumbnail;

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/96f95d00-6f96-4b8a-b84b-010203433d74">Creating Thumbnail Images</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>
 

 

