---
UID: NF:mfidl.IMFSSLCertificateManager.BeginGetClientCertificate
title: IMFSSLCertificateManager::BeginGetClientCertificate
author: windows-sdk-content
description: Starts an asynchronous call to get the client SSL certificate.
old-location: mf\imfsslcertificatemanager_begingetclientcertificate.htm
tech.root: medfound
ms.assetid: e375cb97-bb43-4852-9671-dd8fdea34cef
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: BeginGetClientCertificate, BeginGetClientCertificate method [Media Foundation], BeginGetClientCertificate method [Media Foundation],IMFSSLCertificateManager interface, IMFSSLCertificateManager interface [Media Foundation],BeginGetClientCertificate method, IMFSSLCertificateManager.BeginGetClientCertificate, IMFSSLCertificateManager::BeginGetClientCertificate, mf.imfsslcertificatemanager_begingetclientcertificate, mfidl/IMFSSLCertificateManager::BeginGetClientCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFSSLCertificateManager.BeginGetClientCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSSLCertificateManager::BeginGetClientCertificate


## -description


Starts an asynchronous call to get the client SSL certificate.


## -parameters




### -param pszURL [in]

A null-terminated string that contains the URL for which a client-side SSL certificate is required. Media Foundation can  resolve the scheme and send the request to the server.


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param pState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked. 




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/25cd2ab0-7f58-4bd5-b594-75a3acbdc2d9">IMFSSLCertificateManager::EndGetClientCertificate</a> to complete the asynchronous request. 






## -see-also




<a href="https://msdn.microsoft.com/1d8688a5-d476-457d-a0ad-e4f106ac3484">Calling Asynchronous Methods</a>



<a href="https://msdn.microsoft.com/62e4227d-6bc9-4011-acee-6278fe388830">IMFSSLCertificateManager</a>
 

 

