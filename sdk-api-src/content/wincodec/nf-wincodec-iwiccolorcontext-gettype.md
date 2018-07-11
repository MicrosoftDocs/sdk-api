---
UID: NF:wincodec.IWICColorContext.GetType
title: IWICColorContext::GetType
author: windows-sdk-content
description: Retrieves the color context type.
old-location: wic\_wic_codec_iwiccolorcontext_gettype.htm
old-project: wic
ms.assetid: 34b23e94-bf6a-4440-825f-3997658e0095
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetType, GetType method [Windows Imaging Component], GetType method [Windows Imaging Component],IWICColorContext interface, IWICColorContext interface [Windows Imaging Component],GetType method, IWICColorContext.GetType, IWICColorContext::GetType, _wic_codec_iwiccolorcontext_gettype, wic._wic_codec_iwiccolorcontext_gettype, wincodec/IWICColorContext::GetType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICColorContext.GetType
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICColorContext::GetType


## -description


Retrieves the color context type.


## -parameters




### -param pType [out]

Type: <b><a href="https://msdn.microsoft.com/30fab53b-8edf-488c-a6f2-5224b94e0500">WICColorContextType</a>*</b>

A pointer that receives the <a href="https://msdn.microsoft.com/30fab53b-8edf-488c-a6f2-5224b94e0500">WICColorContextType</a> of the color context.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



