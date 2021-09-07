---
UID: NF:mfidl.IMFSSLCertificateManager.OnServerCertificate
title: IMFSSLCertificateManager::OnServerCertificate (mfidl.h)
description: Called by Media Foundation when the server SSL certificate has been received; indicates whether the server certificate is accepted.
helpviewer_keywords: ["IMFSSLCertificateManager interface [Media Foundation]","OnServerCertificate method","IMFSSLCertificateManager.OnServerCertificate","IMFSSLCertificateManager::OnServerCertificate","OnServerCertificate","OnServerCertificate method [Media Foundation]","OnServerCertificate method [Media Foundation]","IMFSSLCertificateManager interface","mf.imfsslcertificatemanager_onservercertificate","mfidl/IMFSSLCertificateManager::OnServerCertificate"]
old-location: mf\imfsslcertificatemanager_onservercertificate.htm
tech.root: mf
ms.assetid: 4ba43175-4429-437d-acfb-e0ea8d300651
ms.date: 12/05/2018
ms.keywords: IMFSSLCertificateManager interface [Media Foundation],OnServerCertificate method, IMFSSLCertificateManager.OnServerCertificate, IMFSSLCertificateManager::OnServerCertificate, OnServerCertificate, OnServerCertificate method [Media Foundation], OnServerCertificate method [Media Foundation],IMFSSLCertificateManager interface, mf.imfsslcertificatemanager_onservercertificate, mfidl/IMFSSLCertificateManager::OnServerCertificate
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
 - IMFSSLCertificateManager::OnServerCertificate
 - mfidl/IMFSSLCertificateManager::OnServerCertificate
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
 - IMFSSLCertificateManager.OnServerCertificate
---

# IMFSSLCertificateManager::OnServerCertificate


## -description

Called by Media Foundation when the server SSL certificate has been received; indicates whether the server certificate is accepted.

## -parameters

### -param pszURL [in]

Pointer to a string that contains the URL used to send the request to the server, and for which a server-side SSL certificate has been received.

### -param pbData [in]

Pointer to a buffer that contains the server SSL certificate.

### -param cbData [in]

Pointer to a <b>DWORD</b> variable that indicates the size of <i>pbData</i> in bytes.

### -param pfIsGood [out]

Pointer to a <b>BOOL</b> variable that indicates whether the certificate is accepted.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager">IMFSSLCertificateManager</a>