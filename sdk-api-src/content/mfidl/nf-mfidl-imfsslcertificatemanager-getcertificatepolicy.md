---
UID: NF:mfidl.IMFSSLCertificateManager.GetCertificatePolicy
title: IMFSSLCertificateManager::GetCertificatePolicy (mfidl.h)
author: windows-sdk-content
description: Indicates whether the server SSL certificate must be verified by the caller, Media Foundation, or the IMFSSLCertificateManager implementation class.
old-location: mf\imfsslcertificatemanager_getcertificatepolicy.htm
tech.root: medfound
ms.assetid: 343f86ca-0036-4324-b3ca-4dba8fbc26a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCertificatePolicy, GetCertificatePolicy method [Media Foundation], GetCertificatePolicy method [Media Foundation],IMFSSLCertificateManager interface, IMFSSLCertificateManager interface [Media Foundation],GetCertificatePolicy method, IMFSSLCertificateManager.GetCertificatePolicy, IMFSSLCertificateManager::GetCertificatePolicy, mf.imfsslcertificatemanager_getcertificatepolicy, mfidl/IMFSSLCertificateManager::GetCertificatePolicy
ms.topic: method
f1_keywords: ["mfidl/IMFSSLCertificateManager.GetCertificatePolicy"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSSLCertificateManager.GetCertificatePolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSSLCertificateManager::GetCertificatePolicy


## -description


Indicates whether the server SSL certificate must be verified by the caller, Media Foundation,  or the <b>IMFSSLCertificateManager</b> implementation class.


## -parameters




### -param pszURL [in]

 Pointer to a string that contains the URL that  is sent to the server.


### -param pfOverrideAutomaticCheck [out]

Pointer to a <b>BOOL</b> value. Set to <b>TRUE</b> if <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsslcertificatemanager-onservercertificate">IMFSSLCertificateManager::OnServerCertificate</a> is used to verify the server certificate.
Set to <b>FALSE</b> if Media Foundation verifies the server certificate  by using the certificates in the Windows certificate store.



### -param pfClientCertificateAvailable [out]

Pointer to a <b>BOOL</b> value. Set to <b>TRUE</b> if the SSL certificate for the client is available for immediate retrieval. Media Foundation  calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsslcertificatemanager-begingetclientcertificate">IMFSSLCertificateManager::GetClientCertificate</a> to obtain the client certificate synchronously. If the value is set to <b>FALSE</b>, Media Foundation obtains the client SSL certificate with an asynchronous call to <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsslcertificatemanager-begingetclientcertificate">IMFSSLCertificateManager::BeginGetClientCertificate</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager">IMFSSLCertificateManager</a>
 

 

