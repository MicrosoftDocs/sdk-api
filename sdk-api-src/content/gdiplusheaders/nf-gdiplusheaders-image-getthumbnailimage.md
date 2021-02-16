---
UID: NF:gdiplusheaders.Image.GetThumbnailImage
title: Image::GetThumbnailImage (gdiplusheaders.h)
description: The Image::GetThumbnailImage method gets a thumbnail image from this Image object.
helpviewer_keywords: ["GetThumbnailImage","GetThumbnailImage method [GDI+]","GetThumbnailImage method [GDI+]","Image class","Image class [GDI+]","GetThumbnailImage method","Image.GetThumbnailImage","Image::GetThumbnailImage","_gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_","gdiplus._gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getthumbnailimage.htm
ms.date: 12/05/2018
ms.keywords: GetThumbnailImage, GetThumbnailImage method [GDI+], GetThumbnailImage method [GDI+],Image class, Image class [GDI+],GetThumbnailImage method, Image.GetThumbnailImage, Image::GetThumbnailImage, _gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_, gdiplus._gdiplus_CLASS_Image_GetThumbnailImage_thumbWidth_thumbHeight_callback_callbackData_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Image::GetThumbnailImage
 - gdiplusheaders/Image::GetThumbnailImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetThumbnailImage
---

# Image::GetThumbnailImage


## -description

The <b>Image::GetThumbnailImage</b> method gets a thumbnail image from this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

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

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

This method returns a pointer to an 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that contains the thumbnail image.

## -remarks

A thumbnail image is a small copy of an image. Some image files have a thumbnail image embedded in the file. In such cases, this method retrieves the embedded thumbnail image. If there is no embedded thumbnail image, this method creates a thumbnail image by scaling the main image to the size specified in the 
				<i>thumbWidth</i> and 
				<i>thumbHeight</i> parameters. If both of those parameters are 0, a system-defined size is used.


#### Examples



The following example creates an 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a JPEG file. The code calls the <b>Image::GetThumbnailImage</b> method of that 
						<b>Image</b> object and then displays the thumbnail image along with the main image.


```cpp
VOID Example_GetThumbnail(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an image and a thumbnail of the image.
   Image image(L"Crayons.jpg");
   Image* pThumbnail = image.GetThumbnailImage(40, 40, NULL, NULL);

   // Draw the original and the thumbnail images.
   graphics.DrawImage(&image, 10, 10, image.GetWidth(), image.GetHeight());
   graphics.DrawImage(
      pThumbnail, 
      150, 
      10, 
      pThumbnail->GetWidth(), 
      pThumbnail->GetHeight());

   delete pThumbnail;

}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-thumbnail-images-use">Creating Thumbnail Images</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>