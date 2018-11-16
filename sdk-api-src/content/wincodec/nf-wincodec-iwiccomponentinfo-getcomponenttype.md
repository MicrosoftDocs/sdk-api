---
UID: NF:wincodec.IWICComponentInfo.GetComponentType
title: IWICComponentInfo::GetComponentType
author: windows-sdk-content
description: Retrieves the component's WICComponentType.
old-location: wic\_wic_codec_iwiccomponentinfo_getcomponenttype.htm
tech.root: wic
ms.assetid: e7599299-2854-4796-8760-740a6ae7ad4f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetComponentType, GetComponentType method [Windows Imaging Component], GetComponentType method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetComponentType method, IWICComponentInfo.GetComponentType, IWICComponentInfo::GetComponentType, _wic_codec_iwiccomponentinfo_getcomponenttype, wic._wic_codec_iwiccomponentinfo_getcomponenttype, wincodec/IWICComponentInfo::GetComponentType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICComponentInfo.GetComponentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICComponentInfo.GetComponentType
: 
---

# IWICComponentInfo::GetComponentType


## -description


Retrieves the component's <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>.


## -parameters




### -param pType [out]

Type: <b><a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>*</b>

A pointer that receives the <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



