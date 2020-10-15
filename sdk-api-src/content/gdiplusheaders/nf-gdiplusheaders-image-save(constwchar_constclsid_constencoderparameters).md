---
UID: NF:gdiplusheaders.Image.Save(constWCHAR,constCLSID,constEncoderParameters)
title: Image::Save
description: The Image::Save method saves this image to a file.
tech.root: gdiplus
helpviewer_keywords: ["Image::Save"]
ms.assetid: e2c57259-fe82-40dc-86a3-3f4110e6c0ee
ms.date: 05/20/2019
ms.keywords: Image::Save
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusheaders.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Image::Save
 - gdiplusheaders/Image::Save
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Image::Save
---

# Image::Save(WCHAR*,CLSID*,EncoderParameters*)


## -description

The **Image::Save** method saves this image to a file.

## -parameters

### -param filename

Pointer to a null-terminated string that specifies the path name for the saved image.

### -param clsidEncoder

Pointer to a CLSID that specifies the encoder to use to save the image.

### -param encoderParams

Optional.
Pointer to an <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object that holds parameters used by the encoder.
The default value is **NULL**.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

GDI+ does not allow you to save an image to the same file that you used to construct the image.
The following code creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object by passing the file name `MyImage.jpg` to an **Image** constructor.
That same file name is passed to the **Image::Save** method of the Image object, so the **Image::Save** method fails.

```cpp
Image image(L"myImage.jpg");

// Do other operations.

// Save the image to the same file name. (This operation will fail.)
image.Save(L"myImage.jpg", ...);
```

#### Examples

The following example creates an **Image** object from a PNG file and then creates a Graphics object based on that **Image** object.
The code draws the image, alters the image, and draws the image again.
Finally, the code saves the altered image to a file.

The code relies on a helper function, *GetEncoderClsid*, to get the class identifier for the PNG encoder.
The *GetEncoderClsid* function is shown in *Retrieving the Class Identifier for an Encoder*.

The technique of constructing a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object based on an image works only for certain image formats.
For example, you cannot construct a **Graphics** object based on an image that has a color depth of 4 bits per pixel.
For more information about which formats are supported by the **Graphics** constructor, see <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>.

```cpp
VOID Example_SaveFile(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a PNG file.
   Image  image(L"Mosaic.png");

   // Draw the image.
   graphics.DrawImage(&image, 10, 10);

   // Construct a Graphics object based on the image.
   Graphics imageGraphics(&image);

   // Alter the image.
   SolidBrush brush(Color(255, 0, 0, 255));
   imageGraphics.FillEllipse(&brush, 20, 30, 80, 50);

   // Draw the altered image.
   graphics.DrawImage(&image, 200, 10);

   // Save the altered image.
   CLSID pngClsid;
   GetEncoderClsid(L"image/png", &pngClsid);
   image.Save(L"Mosaic2.png", &pngClsid, NULL);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>

<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>

<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>

<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)">Image::Save Methods</a>

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)">Image::SaveAdd Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>