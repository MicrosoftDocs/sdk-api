---
UID: NF:gdiplusheaders.Image.Save(IN IStream,IN const CLSID,IN const EncoderParameters)
title: Image::Save(IN IStream,IN const CLSID,IN const EncoderParameters)
author: windows-sdk-content
description: The Image::Save method saves this image to a stream.
old-location: gdiplus\_gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\imagesavemethods\save_32stream_clsidencoder_encoderparams.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Image class [GDI+],Save method, Image.Save, Image.Save(IN IStream,IN const CLSID,IN const EncoderParameters), Image.Save(IStream*,const CLSID*,const EncoderParameters*), Image::Save, Image::Save(IN IStream,IN const CLSID,IN const EncoderParameters), Save, Save method [GDI+], Save method [GDI+],Image class, _gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_, gdiplus._gdiplus_CLASS_Image_Save_stream_clsidEncoder_encoderParams_
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
 - Image.Save
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::Save(IN IStream,IN const CLSID,IN const EncoderParameters)


## -description


The <b>Image::Save</b> method saves this image to a stream.


## -parameters




### -param stream [in]

Type: <b><a href="_stg_istream">IStream</a>*</b>

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

Type: <b>const <a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>*</b>

Optional. Pointer to an <a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a> object that holds parameters used by the encoder. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Do not save an image to the same stream that was used to construct the image. Doing so might damage the stream.



<pre class="syntax" xml:space="preserve"><code>Image image(myStream); 
...
image.Save(myStream, ...); // Do not do this.</code></pre>

#### Examples

The following example creates two 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> objects: one constructed from a JPEG file and one constructed from a PNG file. The code creates a compound file with two streams and saves the two images to those streams.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Status MakeCompoundFile()
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
      &amp;pIStorage);

   if(FAILED(hr))
      goto Exit;

   // Create a stream in the compound file.
   hr = pIStorage-&gt;CreateStream(
      L"StreamImage1",
      STGM_READWRITE|STGM_SHARE_EXCLUSIVE,
      0,
      0,
      &amp;pIStream1);

   if(FAILED(hr))
      goto Exit;

   // Create a second stream in the compound file.
   hr = pIStorage-&gt;CreateStream(
      L"StreamImage2",
      STGM_READWRITE|STGM_SHARE_EXCLUSIVE,
      0,
      0,
      &amp;pIStream2);

   if(FAILED(hr))
      goto Exit;

   // Get the class identifier for the JPEG encoder.
   CLSID jpgClsid;
   GetEncoderClsid(L"image/jpeg", &amp;jpgClsid);

   // Get the class identifier for the PNG encoder.
   CLSID pngClsid;
   GetEncoderClsid(L"image/png", &amp;pngClsid);

   // Save image1 as a stream in the compound file.
   stat = image1.Save(pIStream1, &amp;jpgClsid);
   if(stat != Ok)
      goto Exit;

   // Save image2 as a stream in the compound file.
   stat = image2.Save(pIStream2, &amp;pngClsid);

Exit:
   if(pIStream1)
      pIStream1-&gt;Release(); 
   if(pIStream2)
      pIStream2-&gt;Release();
   if(pIStorage)
      pIStorage-&gt;Release();

   if(stat != Ok || FAILED(hr))
      return GenericError;

   return Ok;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>



<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/b017e3d1-2faa-4d79-b1d8-8775b7be2dad">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ea264188-3c39-4f00-84f3-114c81a5642e">Image::Save Methods</a>



<a href="https://msdn.microsoft.com/e597f6e6-6e07-4afb-8905-26e4af961685">Image::SaveAdd Methods</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

