---
UID: NF:wincodec.IWICComponentInfo.GetVersion
title: IWICComponentInfo::GetVersion
author: windows-sdk-content
description: Retrieves the component's version.
old-location: wic\_wic_codec_iwiccomponentinfo_getversion.htm
old-project: wic
ms.assetid: f65d13ae-ccec-49a8-8818-225464b3a117
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetVersion, GetVersion method [Windows Imaging Component], GetVersion method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetVersion method, IWICComponentInfo.GetVersion, IWICComponentInfo::GetVersion, _wic_codec_iwiccomponentinfo_getversion, wic._wic_codec_iwiccomponentinfo_getversion, wincodec/IWICComponentInfo::GetVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICComponentInfo.GetVersion
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentInfo::GetVersion


## -description


Retrieves the component's version. 


## -parameters




### -param cchVersion [in]

Type: <b>UINT</b>

The size of the <i>wzVersion</i> buffer.


### -param wzVersion [in, out]

Type: <b>WCHAR*</b>

A pointer that receives a culture invariant string of the component's version.


### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's version. The version is optional; if a value is not specified by the component, the length returned is 0.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



All built-in components return "1.0.0.0", except for pixel formats, which do not have a version.

If <i>cchAuthor</i> is 0 and <i>wzAuthor</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.



