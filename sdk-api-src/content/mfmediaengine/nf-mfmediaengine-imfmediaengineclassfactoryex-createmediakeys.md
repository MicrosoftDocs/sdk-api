---
UID: NF:mfmediaengine.IMFMediaEngineClassFactoryEx.CreateMediaKeys
title: IMFMediaEngineClassFactoryEx::CreateMediaKeys (mfmediaengine.h)
author: windows-sdk-content
description: Creates a media keys object based on the specified key system.
old-location: mf\imfmediaengineclassfactoryex_createmediakeys.htm
tech.root: medfound
ms.assetid: 40b2b978-f12c-4066-acf5-e0c68b0fa928
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateMediaKeys, CreateMediaKeys method [Media Foundation], CreateMediaKeys method [Media Foundation],IMFMediaEngineClassFactoryEx interface, IMFMediaEngineClassFactoryEx interface [Media Foundation],CreateMediaKeys method, IMFMediaEngineClassFactoryEx.CreateMediaKeys, IMFMediaEngineClassFactoryEx::CreateMediaKeys, mf.imfmediaengineclassfactoryex_createmediakeys, mfmediaengine/IMFMediaEngineClassFactoryEx::CreateMediaKeys
ms.topic: method
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
 - IMFMediaEngineClassFactoryEx.CreateMediaKeys
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineClassFactoryEx::CreateMediaKeys


## -description


Creates a media keys object based on the specified key system.


## -parameters




### -param keySystem

The media keys system.


### -param cdmStorePath

Points to a location to store Content Decryption Module (CDM) data which might be locked by multiple process and so might be incompatible with store app suspension.


### -param ppKeys

The media keys.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Checks if <i>keySystem</i> is a supported key system and creates the related Content Decryption Module (CDM).





## -see-also




<a href="https://msdn.microsoft.com/d672ee59-f702-49c7-8ccf-5ba0260c9b23">IMFMediaEngineClassFactoryEx</a>
 

 

