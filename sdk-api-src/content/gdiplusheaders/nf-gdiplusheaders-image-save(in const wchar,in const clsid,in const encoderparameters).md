---
UID: NF:gdiplusheaders.Image.Save(IN const WCHAR,IN const CLSID,IN const EncoderParameters)
title: Image::Save(IN const WCHAR,IN const CLSID,IN const EncoderParameters)
author: windows-sdk-content
description: The Image::Save method saves this image to a file.
old-location: gdiplus\_gdiplus_CLASS_Image_Save_filename_clsidEncoder_encoderParams_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\imagesavemethods\save_39filename_clsidencoder_encoderparams.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Image class [GDI+],Save method, Image.Save, Image.Save(IN const WCHAR,IN const CLSID,IN const EncoderParameters), Image.Save(const WCHAR*,const CLSID*,const EncoderParameters*), Image::Save, Image::Save(IN const WCHAR,IN const CLSID,IN const EncoderParameters), Save, Save method [GDI+], Save method [GDI+],Image class, _gdiplus_CLASS_Image_Save_filename_clsidEncoder_encoderParams_, gdiplus._gdiplus_CLASS_Image_Save_filename_clsidEncoder_encoderParams_
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

# Image::Save(IN const WCHAR,IN const CLSID,IN const EncoderParameters)


## -description


The <b>Image::Save</b> method saves this image to a file.


## -parameters




### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a null-terminated string that specifies the path name for the saved image. 


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



GDI+ does not allow you to save an image to the same file that you used to construct the image. The following code creates an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object by passing the file name MyImage.jpg to an 
				<b>Image</b> constructor. That same file name is passed to the <b>Image::Save</b> method of the 
				<b>Image</b> object, so the <b>Image::Save</b> method fails.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Image image(L"myImage.jpg"); 

// Do other operations.

// Save the image to the same file name. (This operation will fail.)
image.Save(L"myImage.jpg", ...); </pre>
</td>
</tr>
</table></span></div>

#### Examples

The following example creates an 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object from a PNG file and then creates a 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object based on that 
						<b>Image</b> object. The code draws the image, alters the image, and draws the image again. Finally, the code saves the altered image to a file.

The code relies on a helper function, GetEncoderClsid, to get the class identifier for the PNG encoder. The GetEncoderClsid function is shown in <a href="https://msdn.microsoft.com/f78dac7c-4bc1-4614-8a26-d99d5619399a">Retrieving the Class Identifier for an Encoder</a>.

The technique of constructing a 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object based on an image works only for certain image formats. For example, you cannot construct a 
						<b>Graphics</b> object based on an image that has a color depth of 4 bits per pixel. For more information about which formats are supported by the 
						<b>Graphics</b> constructor, see <a href="https://msdn.microsoft.com/3e63938f-f16d-4d83-bffa-e015da9d35cf">Graphics</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SaveFile(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an Image object based on a PNG file.
   Image  image(L"Mosaic.png");

   // Draw the image.
   graphics.DrawImage(&amp;image, 10, 10);

   // Construct a Graphics object based on the image.
   Graphics imageGraphics(&amp;image);

   // Alter the image.
   SolidBrush brush(Color(255, 0, 0, 255));
   imageGraphics.FillEllipse(&amp;brush, 20, 30, 80, 50);

   // Draw the altered image.
   graphics.DrawImage(&amp;image, 200, 10);

   // Save the altered image.
   CLSID pngClsid;
   GetEncoderClsid(L"image/png", &amp;pngClsid);
   image.Save(L"Mosaic2.png", &amp;pngClsid, NULL);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>



<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ea264188-3c39-4f00-84f3-114c81a5642e">Image::Save Methods</a>



<a href="https://msdn.microsoft.com/e597f6e6-6e07-4afb-8905-26e4af961685">Image::SaveAdd Methods</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

