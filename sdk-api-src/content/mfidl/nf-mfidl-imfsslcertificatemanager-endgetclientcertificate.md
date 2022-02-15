---
UID: NF:mfidl.IMFSSLCertificateManager.EndGetClientCertificate
title: IMFSSLCertificateManager::EndGetClientCertificate (mfidl.h)
description: Completes an asynchronous request to get the client SSL certificate.
helpviewer_keywords: ["EndGetClientCertificate","EndGetClientCertificate method [Media Foundation]","EndGetClientCertificate method [Media Foundation]","IMFSSLCertificateManager interface","IMFSSLCertificateManager interface [Media Foundation]","EndGetClientCertificate method","IMFSSLCertificateManager.EndGetClientCertificate","IMFSSLCertificateManager::EndGetClientCertificate","mf.imfsslcertificatemanager_endgetclientcertificate","mfidl/IMFSSLCertificateManager::EndGetClientCertificate"]
old-location: mf\imfsslcertificatemanager_endgetclientcertificate.htm
tech.root: mf
ms.assetid: 25cd2ab0-7f58-4bd5-b594-75a3acbdc2d9
ms.date: 12/05/2018
ms.keywords: EndGetClientCertificate, EndGetClientCertificate method [Media Foundation], EndGetClientCertificate method [Media Foundation],IMFSSLCertificateManager interface, IMFSSLCertificateManager interface [Media Foundation],EndGetClientCertificate method, IMFSSLCertificateManager.EndGetClientCertificate, IMFSSLCertificateManager::EndGetClientCertificate, mf.imfsslcertificatemanager_endgetclientcertificate, mfidl/IMFSSLCertificateManager::EndGetClientCertificate
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
 - IMFSSLCertificateManager::EndGetClientCertificate
 - mfidl/IMFSSLCertificateManager::EndGetClientCertificate
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
 - IMFSSLCertificateManager.EndGetClientCertificate
---

# IMFSSLCertificateManager::EndGetClientCertificate


## -description

Completes an asynchronous request to get the client SSL certificate.

## -parameters

### -param pResult [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

### -param ppbData [out]

Receives a pointer to the buffer that stores the certificate.
The caller must free the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbData [out]

Receives the size of the <i>ppbData</i> buffer, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method after the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsslcertificatemanager-begingetclientcertificate">IMFSSLCertificateManager::BeginGetClientCertificate</a> method completes asynchronously.

## -see-also

<a href="/windows/desktop/medfound/calling-asynchronous-methods">Calling Asynchronous Methods</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager">IMFSSLCertificateManager</a>