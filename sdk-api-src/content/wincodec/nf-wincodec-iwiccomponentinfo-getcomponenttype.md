---
UID: NF:wincodec.IWICComponentInfo.GetComponentType
title: IWICComponentInfo::GetComponentType method
author: windows-driver-content
description: Retrieves the component's WICComponentType.
old-location: wic\_wic_codec_iwiccomponentinfo_getcomponenttype.htm
old-project: wic
ms.assetid: e7599299-2854-4796-8760-740a6ae7ad4f
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetComponentType method [Windows Imaging Component], GetComponentType method [Windows Imaging Component], IWICComponentInfo interface, GetComponentType,IWICComponentInfo.GetComponentType, IWICComponentInfo, IWICComponentInfo interface [Windows Imaging Component], GetComponentType method, IWICComponentInfo::GetComponentType, _wic_codec_iwiccomponentinfo_getcomponenttype, wic._wic_codec_iwiccomponentinfo_getcomponenttype, wincodec/IWICComponentInfo::GetComponentType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	IWICComponentInfo.GetComponentType
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentInfo::GetComponentType method


## -description


Retrieves the component's <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>.


## -parameters




### -param pType [out]

Type: <b><a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>*</b>

A pointer that receives the <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



