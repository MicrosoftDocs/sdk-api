---
UID: NF:mfidl.IMFSSLCertificateManager.BeginGetClientCertificate
title: IMFSSLCertificateManager::BeginGetClientCertificate (mfidl.h)
description: Starts an asynchronous call to get the client SSL certificate.
helpviewer_keywords: ["BeginGetClientCertificate","BeginGetClientCertificate method [Media Foundation]","BeginGetClientCertificate method [Media Foundation]","IMFSSLCertificateManager interface","IMFSSLCertificateManager interface [Media Foundation]","BeginGetClientCertificate method","IMFSSLCertificateManager.BeginGetClientCertificate","IMFSSLCertificateManager::BeginGetClientCertificate","mf.imfsslcertificatemanager_begingetclientcertificate","mfidl/IMFSSLCertificateManager::BeginGetClientCertificate"]
old-location: mf\imfsslcertificatemanager_begingetclientcertificate.htm
tech.root: mf
ms.assetid: e375cb97-bb43-4852-9671-dd8fdea34cef
ms.date: 12/05/2018
ms.keywords: BeginGetClientCertificate, BeginGetClientCertificate method [Media Foundation], BeginGetClientCertificate method [Media Foundation],IMFSSLCertificateManager interface, IMFSSLCertificateManager interface [Media Foundation],BeginGetClientCertificate method, IMFSSLCertificateManager.BeginGetClientCertificate, IMFSSLCertificateManager::BeginGetClientCertificate, mf.imfsslcertificatemanager_begingetclientcertificate, mfidl/IMFSSLCertificateManager::BeginGetClientCertificate
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFSSLCertificateManager::BeginGetClientCertificate
 - mfidl/IMFSSLCertificateManager::BeginGetClientCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSSLCertificateManager.BeginGetClientCertificate
---

# IMFSSLCertificateManager::BeginGetClientCertificate


## -description

Starts an asynchronous call to get the client SSL certificate.

## -parameters

### -param pszURL [in]

A null-terminated string that contains the URL for which a client-side SSL certificate is required. Media Foundation can  resolve the scheme and send the request to the server.

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the operation completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsslcertificatemanager-endgetclientcertificate">IMFSSLCertificateManager::EndGetClientCertificate</a> to complete the asynchronous request.

## -see-also

<a href="/windows/desktop/medfound/calling-asynchronous-methods">Calling Asynchronous Methods</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager">IMFSSLCertificateManager</a>