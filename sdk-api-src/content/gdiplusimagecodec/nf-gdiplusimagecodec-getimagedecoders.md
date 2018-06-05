---
UID: NF:gdiplusimagecodec.GetImageDecoders
title: GetImageDecoders function
author: windows-sdk-content
description: The GetImageDecoders function gets an array of ImageCodecInfo objects that contain information about the available image decoders.
old-location: gdiplus\_gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimagedecoders.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetImageDecoders, GetImageDecoders function [GDI+], _gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_, gdiplus._gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_, gdiplusimagecodec/GetImageDecoders
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	GetImageDecoders
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# GetImageDecoders function


## -description


The <b>GetImageDecoders</b> function gets an array of <a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects that contain information about the available image decoders.


## -parameters




### -param numDecoders [in]

Type: <b>UINT</b>

Integer that specifies the number of available image decoders. Call <a href="https://msdn.microsoft.com/2e0a6811-43be-417f-9bc8-ed39d27c8bec">GetImageDecodersSize</a> to determine this number. 


### -param size [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the array of 
					<a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects. Call <a href="https://msdn.microsoft.com/2e0a6811-43be-417f-9bc8-ed39d27c8bec">GetImageDecodersSize</a> to determine this number. 


### -param decoders [out]

Type: <b><a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a>*</b>

Pointer to a buffer that receives the array of 
					<a href="https://msdn.microsoft.com/b644b207-0b87-48d3-9db9-37b7c2e43b93">ImageCodecInfo</a> objects. You must allocate memory for this buffer. Call <a href="https://msdn.microsoft.com/2e0a6811-43be-417f-9bc8-ed39d27c8bec">GetImageDecodersSize</a> to determine the size of the required buffer. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/2e0a6811-43be-417f-9bc8-ed39d27c8bec">GetImageDecodersSize</a>



<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/b017e3d1-2faa-4d79-b1d8-8775b7be2dad">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

