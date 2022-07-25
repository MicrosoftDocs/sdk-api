---
UID: NF:mfidl.IMFSourceResolver.CancelObjectCreation
title: IMFSourceResolver::CancelObjectCreation (mfidl.h)
description: Cancels an asynchronous request to create an object.
helpviewer_keywords: ["6a30ac92-a281-4293-8975-987fa25a5318","CancelObjectCreation","CancelObjectCreation method [Media Foundation]","CancelObjectCreation method [Media Foundation]","IMFSourceResolver interface","IMFSourceResolver interface [Media Foundation]","CancelObjectCreation method","IMFSourceResolver.CancelObjectCreation","IMFSourceResolver::CancelObjectCreation","mf.imfsourceresolver_cancelobjectcreation","mfidl/IMFSourceResolver::CancelObjectCreation"]
old-location: mf\imfsourceresolver_cancelobjectcreation.htm
tech.root: mf
ms.assetid: 6a30ac92-a281-4293-8975-987fa25a5318
ms.date: 12/05/2018
ms.keywords: 6a30ac92-a281-4293-8975-987fa25a5318, CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],CancelObjectCreation method, IMFSourceResolver.CancelObjectCreation, IMFSourceResolver::CancelObjectCreation, mf.imfsourceresolver_cancelobjectcreation, mfidl/IMFSourceResolver::CancelObjectCreation
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceResolver::CancelObjectCreation
 - mfidl/IMFSourceResolver::CancelObjectCreation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceResolver.CancelObjectCreation
---

# IMFSourceResolver::CancelObjectCreation


## -description

Cancels an asynchronous request to create an object.

## -parameters

### -param pIUnknownCancelCookie [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream">IMFSourceResolver::BeginCreateObjectFromByteStream</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl">IMFSourceResolver::BeginCreateObjectFromURL</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use this method to cancel a previous call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream">BeginCreateObjectFromByteStream</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl">BeginCreateObjectFromURL</a>. Because these methods are asynchronous, however, they might be completed before the operation can be canceled. Therefore, your callback might still be invoked after you call this method.
      

<div class="alert"><b>Note</b>  This method cannot be called remotely.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>