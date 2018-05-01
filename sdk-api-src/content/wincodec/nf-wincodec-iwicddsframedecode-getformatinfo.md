---
UID: NF:wincodec.IWICDdsFrameDecode.GetFormatInfo
title: IWICDdsFrameDecode::GetFormatInfo method
author: windows-driver-content
description: Gets information about the format in which the DDS image is stored.
old-location: wic\iwicddsframedecode_getformatinfo.htm
old-project: wic
ms.assetid: 0D5B9E45-E1EA-4D16-B793-63FEAB2BAF65
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetFormatInfo method [Windows Imaging Component], GetFormatInfo method [Windows Imaging Component], IWICDdsFrameDecode interface, GetFormatInfo,IWICDdsFrameDecode.GetFormatInfo, IWICDdsFrameDecode, IWICDdsFrameDecode interface [Windows Imaging Component], GetFormatInfo method, IWICDdsFrameDecode::GetFormatInfo, wic.iwicddsframedecode_getformatinfo, wincodec/IWICDdsFrameDecode::GetFormatInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICDdsFrameDecode.GetFormatInfo
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDdsFrameDecode::GetFormatInfo method


## -description


Gets information about the format in which the DDS image is stored.


## -parameters




### -param pFormatInfo [out]

Type: <b><a href="https://msdn.microsoft.com/C5F1DA49-EC11-4068-9DC6-D721894371F9">WICDdsFormatInfo</a>*</b>

Information about the DDS format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This information can be used for allocating memory or constructing Direct3D or Direct2D resources, for example by using <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> or <a href="https://msdn.microsoft.com/D1896DEE-4464-48D7-8EFB-18E564E1F88D">ID2D1DeviceContext::CreateBitmap</a>.




## -see-also




<a href="https://msdn.microsoft.com/76741d1e-3e1b-4018-b092-b668ecfd43c9">CreateBitmap</a>



<a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a>



<a href="https://msdn.microsoft.com/52E76A8D-E7E2-46F5-BBCC-B7C74F1B1122">IWICDdsFrameDecode</a>



<a href="https://msdn.microsoft.com/C5F1DA49-EC11-4068-9DC6-D721894371F9">WICDdsFormatInfo</a>
 

 

