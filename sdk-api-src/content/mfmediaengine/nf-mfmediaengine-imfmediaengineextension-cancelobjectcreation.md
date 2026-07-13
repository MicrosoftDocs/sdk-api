---
UID: NF:mfmediaengine.IMFMediaEngineExtension.CancelObjectCreation
title: IMFMediaEngineExtension::CancelObjectCreation (mfmediaengine.h)
description: Cancels the current request to create an object.
helpviewer_keywords: ["CancelObjectCreation","CancelObjectCreation method [Media Foundation]","CancelObjectCreation method [Media Foundation]","IMFMediaEngineExtension interface","IMFMediaEngineExtension interface [Media Foundation]","CancelObjectCreation method","IMFMediaEngineExtension.CancelObjectCreation","IMFMediaEngineExtension::CancelObjectCreation","mf.imfmediaengineextension_cancelobjectcreation","mfmediaengine/IMFMediaEngineExtension::CancelObjectCreation"]
old-location: mf\imfmediaengineextension_cancelobjectcreation.htm
tech.root: mf
ms.assetid: E2FEC865-221E-41B5-8271-32A53D60619E
ms.date: 12/05/2018
ms.keywords: CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],CancelObjectCreation method, IMFMediaEngineExtension.CancelObjectCreation, IMFMediaEngineExtension::CancelObjectCreation, mf.imfmediaengineextension_cancelobjectcreation, mfmediaengine/IMFMediaEngineExtension::CancelObjectCreation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngineExtension::CancelObjectCreation
 - mfmediaengine/IMFMediaEngineExtension::CancelObjectCreation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineExtension.CancelObjectCreation
---

# IMFMediaEngineExtension::CancelObjectCreation


## -description

Cancels the current request to create an object.

## -parameters

### -param pIUnknownCancelCookie [in]

The pointer that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-begincreateobject">IMFMediaEngineExtension::BeginCreateObject</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method attempts to cancel a previous call to <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineextension-begincreateobject">BeginCreateObject</a>. Because that method is asynchronous, however, it might complete before the operation can be canceled.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension">IMFMediaEngineExtension</a>