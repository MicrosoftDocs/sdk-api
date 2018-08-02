---
UID: NF:wincodec.IWICComponentInfo.GetFriendlyName
title: IWICComponentInfo::GetFriendlyName
author: windows-sdk-content
description: Retrieves the component's friendly name, which is a human-readable display name for the component.
old-location: wic\_wic_codec_iwiccomponentinfo_getfriendlyname.htm
old-project: wic
ms.assetid: c67e7a30-8bd5-427b-8a67-c77e3cf86e78
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetFriendlyName, GetFriendlyName method [Windows Imaging Component], GetFriendlyName method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetFriendlyName method, IWICComponentInfo.GetFriendlyName, IWICComponentInfo::GetFriendlyName, _wic_codec_iwiccomponentinfo_getfriendlyname, wic._wic_codec_iwiccomponentinfo_getfriendlyname, wincodec/IWICComponentInfo::GetFriendlyName
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
 - IWICComponentInfo.GetFriendlyName
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentInfo::GetFriendlyName


## -description


Retrieves the component's friendly name, which is a human-readable display name for the component.


## -parameters




### -param cchFriendlyName [in]

Type: <b>UINT</b>

The size of the <i>wzFriendlyName</i> buffer.


### -param wzFriendlyName [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the friendly name of the component.
               The locale of the string depends on the value that the codec wrote to the registry at install time. For built-in components, these strings are always in English.


### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's friendly name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>cchFriendlyName</i> is 0 and <i>wzFriendlyName</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.



