---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory.CreateTimeRange
title: IMFMediaEngineClassFactory::CreateTimeRange (mfmediaengine.h)
author: windows-sdk-content
description: Creates a time range object.
old-location: mf\imfmediaengineclassfactory_createtimerange.htm
tech.root: medfound
ms.assetid: 293769E8-8C8A-40D1-AF51-1DBB773F88D5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateTimeRange, CreateTimeRange method [Media Foundation], CreateTimeRange method [Media Foundation],IMFMediaEngineClassFactory interface, IMFMediaEngineClassFactory interface [Media Foundation],CreateTimeRange method, IMFMediaEngineClassFactory.CreateTimeRange, IMFMediaEngineClassFactory::CreateTimeRange, mf.imfmediaengineclassfactory_createtimerange, mfmediaengine/IMFMediaEngineClassFactory::CreateTimeRange
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineClassFactory.CreateTimeRange"
dev_langs:
 - c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFMediaEngineClassFactory.CreateTimeRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineClassFactory::CreateTimeRange


## -description


Creates a time range object.


## -parameters




### -param ppTimeRange [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory">IMFMediaEngineClassFactory</a>
 

 

