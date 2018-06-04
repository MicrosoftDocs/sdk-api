---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFSSLCertificateManager::GetCertificatePolicy


## -description


Indicates whether the server SSL certificate must be verified by the caller, Media Foundation,  or the <b>IMFSSLCertificateManager</b> implementation class.


## -parameters




### -param pszURL [in]

 Pointer to a string that contains the URL that  is sent to the server.


### -param pfOverrideAutomaticCheck [out]

Pointer to a <b>BOOL</b> value. Set to <b>TRUE</b> if <a href="https://msdn.microsoft.com/4ba43175-4429-437d-acfb-e0ea8d300651">IMFSSLCertificateManager::OnServerCertificate</a> is used to verify the server certificate.
Set to <b>FALSE</b> if Media Foundation verifies the server certificate  by using the certificates in the Windows certificate store.



### -param pfClientCertificateAvailable [out]

Pointer to a <b>BOOL</b> value. Set to <b>TRUE</b> if the SSL certificate for the client is available for immediate retrieval. Media Foundation  calls <a href="https://msdn.microsoft.com/e375cb97-bb43-4852-9671-dd8fdea34cef">IMFSSLCertificateManager::GetClientCertificate</a> to obtain the client certificate synchronously. If the value is set to <b>FALSE</b>, Media Foundation obtains the client SSL certificate with an asynchronous call to <a href="https://msdn.microsoft.com/e375cb97-bb43-4852-9671-dd8fdea34cef">IMFSSLCertificateManager::BeginGetClientCertificate</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62e4227d-6bc9-4011-acee-6278fe388830">IMFSSLCertificateManager</a>
 

 

