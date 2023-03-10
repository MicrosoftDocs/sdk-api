---
UID: NF:gdiplusheaders.Image.SaveAdd(constEncoderParameters)
title: Image::SaveAdd
description: The Image::SaveAdd method adds a frame to a file or stream specified in a previous call to the Save method. (overload 1/2)
tech.root: gdiplus
helpviewer_keywords: ["Image::SaveAdd"]
ms.assetid: 03ebcd9f-83c9-4970-bc89-cfed876de44b
ms.date: 05/20/2019
ms.keywords: Image::SaveAdd
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
 - Image::SaveAdd
 - gdiplusheaders/Image::SaveAdd
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Image::SaveAdd
---

# Image::SaveAdd(EncoderParameters*)


## -description

The **Image::SaveAdd** method adds a frame to a file or stream specified in a previous call to the **Save** method.
Use this method to save selected frames from a multiple-frame image to another multiple-frame image.

## -parameters

### -param encoderParams

Pointer to an <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object that holds parameters required by the image encoder used by the save-add operation.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a TIFF file that has four frames.
The code calls the *Image::SelectActiveFrame* method to navigate to the second frame in the page dimension of that Image object.
(The page dimension is the only dimension in this case.)
Then the code calls the **Save** method to save the second frame to a new file named `TwoFrames.tif`.
The code calls the **Image::SelectActiveFrame** method again to navigate to the fourth frame of the Image object.
Then the code calls the **Image::SaveAdd** method to add the fourth frame to `TwoFrames.tif`.
The code calls the **Image::SaveAdd** method a second time to close `TwoFrames.tif`, and then draws the two frames that were saved in that file.

```cpp
VOID Example_SaveAdd(HDC hdc)
{
   Graphics graphics(hdc);
   EncoderParameters encoderParameters;
   ULONG parameterValue;
   GUID dimension = FrameDimensionPage;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create an image object based on a TIFF file that has four frames.
   Image fourFrames(L"FourFrames.tif");

   // Save the second page (frame).
   parameterValue = EncoderValueMultiFrame;
   fourFrames.SelectActiveFrame(&dimension, 1);
   fourFrames.Save(L"TwoFrames.tif", &encoderClsid, &encoderParameters);

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   fourFrames.SelectActiveFrame(&dimension, 3);
   fourFrames.SaveAdd(&encoderParameters);

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   fourFrames.SaveAdd(&encoderParameters);

   // Draw the two frames of TwoFrames.tif.
   Image twoFrames(L"TwoFrames.tif");
   twoFrames.SelectActiveFrame(&dimension, 0);
   graphics.DrawImage(&twoFrames, 10, 10);
   twoFrames.SelectActiveFrame(&dimension, 1);
   graphics.DrawImage(&twoFrames, 150, 10);
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
