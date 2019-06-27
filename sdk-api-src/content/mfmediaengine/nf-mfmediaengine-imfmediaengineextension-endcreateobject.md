---
UID: NF:mfmediaengine.IMFMediaEngineExtension.EndCreateObject
title: IMFMediaEngineExtension::EndCreateObject (mfmediaengine.h)
author: windows-sdk-content
description: Completes an asynchronous request to create a byte stream or media source.
old-location: mf\imfmediaengineextension_endcreateobject.htm
tech.root: medfound
ms.assetid: F2B19870-7529-4C8C-9FE6-B312F6A2D2ED
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndCreateObject, EndCreateObject method [Media Foundation], EndCreateObject method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],EndCreateObject method, IMFMediaEngineExtension.EndCreateObject, IMFMediaEngineExtension::EndCreateObject, mf.imfmediaengineextension_endcreateobject, mfmediaengine/IMFMediaEngineExtension::EndCreateObject
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineExtension.EndCreateObject"
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
 - IMFMediaEngineExtension.EndCreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineExtension::EndCreateObject


## -description


Completes an asynchronous request to create a byte stream or media source.


## -parameters




### -param pResult [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface.


### -param ppObject [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the byte stream or media source. The caller must release the interface


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Media Engine calls this method to complete the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-begincreateobject">IMFMediaEngineExtension::BeginCreateObject</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension">IMFMediaEngineExtension</a>
 

 

