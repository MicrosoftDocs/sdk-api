---
UID: NF:gdiplusimagecodec.GetImageDecodersSize
title: GetImageDecodersSize function
author: windows-driver-content
description: The GetImageDecodersSize function gets the number of available image decoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageDecoders function.
old-location: gdiplus\_gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimagedecoderssize.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetImageDecodersSize, GetImageDecodersSize function [GDI+], _gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_, gdiplus._gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_, gdiplusimagecodec/GetImageDecodersSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gdiplusimagecodec.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	GetImageDecodersSize
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# GetImageDecodersSize function


## -description


The <b>GetImageDecodersSize</b> function gets the number of available image decoders and the total size of the array of 
			<a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects that is returned by the <a href="https://msdn.microsoft.com/ea9f1436-dafe-4e0d-8cca-81ec262d06a5">GetImageDecoders</a> function.


## -parameters




### -param numDecoders [out]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that receives the number of available image decoders.


### -param size [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of the array of 
					<a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects that is returned by the <a href="https://msdn.microsoft.com/ea9f1436-dafe-4e0d-8cca-81ec262d06a5">GetImageDecoders</a> function. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/ea9f1436-dafe-4e0d-8cca-81ec262d06a5">GetImageDecoders</a>



<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/b017e3d1-2faa-4d79-b1d8-8775b7be2dad">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

