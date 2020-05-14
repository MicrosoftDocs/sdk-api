---
UID: NF:mfmediaengine.IMFMediaEngineClassFactoryEx.IsTypeSupported
title: IMFMediaEngineClassFactoryEx::IsTypeSupported (mfmediaengine.h)
description: Gets a value that indicates if the specified key system supports the specified media type.helpviewer_keywords: ["IMFMediaEngineClassFactoryEx interface [Media Foundation]","IsTypeSupported method","IMFMediaEngineClassFactoryEx.IsTypeSupported","IMFMediaEngineClassFactoryEx::IsTypeSupported","IsTypeSupported","IsTypeSupported method [Media Foundation]","IsTypeSupported method [Media Foundation]","IMFMediaEngineClassFactoryEx interface","mf.imfmediaengineclassfactoryex_istypesupported","mfmediaengine/IMFMediaEngineClassFactoryEx::IsTypeSupported"]
old-location: mf\imfmediaengineclassfactoryex_istypesupported.htm
tech.root: medfound
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineClassFactoryEx interface [Media Foundation],IsTypeSupported method, IMFMediaEngineClassFactoryEx.IsTypeSupported, IMFMediaEngineClassFactoryEx::IsTypeSupported, IsTypeSupported, IsTypeSupported method [Media Foundation], IsTypeSupported method [Media Foundation],IMFMediaEngineClassFactoryEx interface, mf.imfmediaengineclassfactoryex_istypesupported, mfmediaengine/IMFMediaEngineClassFactoryEx::IsTypeSupported
f1_keywords:
- mfmediaengine/IMFMediaEngineClassFactoryEx.IsTypeSupported
dev_langs:
- c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineClassFactoryEx::IsTypeSupported


## -description


Gets a value that indicates if the specified key system supports the specified media type.


## -parameters




### -param type

The MIME type to check support for.


### -param keySystem

The key system to check support for.


### -param isSupported

<b>true</b> if type is supported by <i>keySystem</i>; otherwise, <b>false.</b>


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex">IMFMediaEngineClassFactoryEx</a>
 

 

