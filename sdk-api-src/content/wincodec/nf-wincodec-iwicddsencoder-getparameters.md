---
UID: NF:wincodec.IWICDdsEncoder.GetParameters
title: IWICDdsEncoder::GetParameters
author: windows-sdk-content
description: Gets DDS-specific data.
old-location: wic\iwicddsencoder_getparameters.htm
tech.root: wic
ms.assetid: 2172A086-D0F6-4CFE-849C-A2EF1E89C050
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetParameters, GetParameters method [Windows Imaging Component], GetParameters method [Windows Imaging Component],IWICDdsEncoder interface, IWICDdsEncoder interface [Windows Imaging Component],GetParameters method, IWICDdsEncoder.GetParameters, IWICDdsEncoder::GetParameters, wic.iwicddsencoder_getparameters, wincodec/IWICDdsEncoder::GetParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDdsEncoder.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDdsEncoder::GetParameters


## -description


Gets DDS-specific data.


## -parameters




### -param pParameters [out]

Type: <b><a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>*</b>

Points to the structure where the information is returned.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application can call <b>GetParameters</b> to obtain the default DDS parameters, modify some or all of them, and then call <a href="https://msdn.microsoft.com/9DF51D95-97B0-4EC9-8F77-E49B16D76D77">SetParameters</a>.




## -see-also




<a href="https://msdn.microsoft.com/DF14309F-7595-4ABE-BB6E-03D2914CC86D">IWICDdsEncoder</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

