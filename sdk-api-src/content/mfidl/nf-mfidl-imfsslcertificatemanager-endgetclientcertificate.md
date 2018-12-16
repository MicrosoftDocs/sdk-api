---
UID: NF:mfidl.IMFSSLCertificateManager.EndGetClientCertificate
title: IMFSSLCertificateManager::EndGetClientCertificate
author: windows-sdk-content
description: Completes an asynchronous request to get the client SSL certificate.
old-location: mf\imfsslcertificatemanager_endgetclientcertificate.htm
tech.root: medfound
ms.assetid: 25cd2ab0-7f58-4bd5-b594-75a3acbdc2d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndGetClientCertificate, EndGetClientCertificate method [Media Foundation], EndGetClientCertificate method [Media Foundation],IMFSSLCertificateManager interface, IMFSSLCertificateManager interface [Media Foundation],EndGetClientCertificate method, IMFSSLCertificateManager.EndGetClientCertificate, IMFSSLCertificateManager::EndGetClientCertificate, mf.imfsslcertificatemanager_endgetclientcertificate, mfidl/IMFSSLCertificateManager::EndGetClientCertificate
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
 - IMFSSLCertificateManager.EndGetClientCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSSLCertificateManager::EndGetClientCertificate


## -description


Completes an asynchronous request to get the client SSL certificate.




## -parameters




### -param pResult [in]

A pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. 




### -param ppbData [out]

Receives a pointer to the buffer that stores the certificate.
The caller must free the buffer by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pcbData [out]

Receives the size of the <i>ppbData</i> buffer, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method after the <a href="https://msdn.microsoft.com/e375cb97-bb43-4852-9671-dd8fdea34cef">IMFSSLCertificateManager::BeginGetClientCertificate</a> method completes asynchronously. 




## -see-also




<a href="https://msdn.microsoft.com/1d8688a5-d476-457d-a0ad-e4f106ac3484">Calling Asynchronous Methods</a>



<a href="https://msdn.microsoft.com/62e4227d-6bc9-4011-acee-6278fe388830">IMFSSLCertificateManager</a>
 

 

