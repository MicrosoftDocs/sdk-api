---
UID: NF:gdiplusheaders.Image.Save(IStream,constCLSID,constEncoderParameters)
title: Image::Save(IN IStream,IN const CLSID,IN const EncoderParameters) (gdiplusheaders.h)
description: The Image::Save method saves this image to a stream.
helpviewer_keywords: ["Image class [GDI+]","Save method","Image.Save","Image.Save(IN IStream","IN const CLSID","IN const EncoderParameters)","Image.Save(IStream*","const CLSID*","const EncoderParameters*)","Image::Save","Image::Save(IN IStream","IN const CLSID","IN const EncoderParameters)","Save","Save method [GDI+]","Save method [GDI+]","Image class","_gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_","gdiplus._gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_"]
old-location: gdiplus\_gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\imagesavemethods\save_32stream_clsidencoder_encoderparams.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],Save method, Image.Save, Image.Save(IN IStream,IN const CLSID,IN const EncoderParameters), Image.Save(IStream*,const CLSID*,const EncoderParameters*), Image::Save, Image::Save(IN IStream,IN const CLSID,IN const EncoderParameters), Save, Save method [GDI+], Save method [GDI+],Image class, _gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_, gdiplus._gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_
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
 - Image::Save
 - gdiplusheaders/Image::Save
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
 - Image.Save
---

# Image::Save(IN IStream,IN const CLSID,IN const EncoderParameters)


## -description

The <b>Image::Save</b> method saves this image to a stream.

## -parameters

### -param stream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an 
					<b>IStream</b> COM interface. The implementation of 
					<b>IStream</b> must include the 
					<b>Seek</b>, 
					<b>Read</b>, 
					<b>Write</b>, and 
					<b>Stat</b> methods.

### -param clsidEncoder [in]

Type: <b>const CLSID*</b>

Pointer to a 
					<b>CLSID</b> that specifies the encoder to use to save the image.

### -param encoderParams [in]

Type: <b>const <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>*</b>

Optional. Pointer to an <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object that holds parameters used by the encoder. The default value is <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Do not save an image to the same stream that was used to construct the image. Doing so might damage the stream.




``` syntax
Image image(myStream); 
...
image.Save(myStream, ...); // Do not do this.
```


#### Examples

The following example creates two 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> objects: one constructed from a JPEG file and one constructed from a PNG file. The code creates a compound file with two streams and saves the two images to those streams.


```cpp
Status MakeCompoundFile()
{
   IStorage* pIStorage = NULL;
   IStream* pIStream1 = NULL;
   IStream* pIStream2 = NULL;
   HRESULT hr;
   Status stat = Ok;

   // Create two Image objects from existing files.
   Image image1(L"Crayons.jpg");
   Image image2(L"Mosaic.png");

   hr = CoInitialize(NULL);
   if(FAILED(hr))
      goto Exit;

   // Create a compound file object, and get
   // a pointer to its IStorage interface.
   hr = StgCreateDocfile(
      L"CompoundFile.cmp", 
      STGM_READWRITE|STGM_CREATE|STGM_SHARE_EXCLUSIVE, 
      0, 
      &pIStorage);

   if(FAILED(hr))
      goto Exit;

   // Create a stream in the compound file.
   hr = pIStorage->CreateStream(
      L"StreamImage1",
      STGM_READWRITE|STGM_SHARE_EXCLUSIVE,
      0,
      0,
      &pIStream1);

   if(FAILED(hr))
      goto Exit;

   // Create a second stream in the compound file.
   hr = pIStorage->CreateStream(
      L"StreamImage2",
      STGM_READWRITE|STGM_SHARE_EXCLUSIVE,
      0,
      0,
      &pIStream2);

   if(FAILED(hr))
      goto Exit;

   // Get the class identifier for the JPEG encoder.
   CLSID jpgClsid;
   GetEncoderClsid(L"image/jpeg", &jpgClsid);

   // Get the class identifier for the PNG encoder.
   CLSID pngClsid;
   GetEncoderClsid(L"image/png", &pngClsid);

   // Save image1 as a stream in the compound file.
   stat = image1.Save(pIStream1, &jpgClsid);
   if(stat != Ok)
      goto Exit;

   // Save image2 as a stream in the compound file.
   stat = image2.Save(pIStream2, &pngClsid);

Exit:
   if(pIStream1)
      pIStream1->Release(); 
   if(pIStream2)
      pIStream2->Release();
   if(pIStorage)
      pIStorage->Release();

   if(stat != Ok || FAILED(hr))
      return GenericError;

   return Ok;
}
```

## -see-also

<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>



<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)">Image::Save Methods</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)">Image::SaveAdd Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>
