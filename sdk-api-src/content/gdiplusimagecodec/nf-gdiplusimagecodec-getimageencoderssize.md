---
UID: NF:gdiplusimagecodec.GetImageEncodersSize
title: GetImageEncodersSize function
author: windows-sdk-content
description: The GetImageEncodersSize function gets the number of available image encoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageEncoders function.
old-location: gdiplus\_gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimageencoderssize.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetImageEncodersSize, GetImageEncodersSize function [GDI+], _gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_, gdiplus._gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_, gdiplusimagecodec/GetImageEncodersSize
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
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetImageEncodersSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GetImageEncodersSize function


## -description


The <b>GetImageEncodersSize</b> function gets the number of available image encoders and the total size of the array of 
			<a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects that is returned by the <a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a> function.


## -parameters




### -param numEncoders [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the number of available image encoders. 


### -param size [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of the array of 
					<a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects that is returned by <a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/ea9f1436-dafe-4e0d-8cca-81ec262d06a5">GetImageDecoders</a>



<a href="https://msdn.microsoft.com/2e0a6811-43be-417f-9bc8-ed39d27c8bec">GetImageDecodersSize</a>



<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

