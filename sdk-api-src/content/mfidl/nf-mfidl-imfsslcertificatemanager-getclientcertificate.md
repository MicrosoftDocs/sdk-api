---
UID: NF:mfidl.IMFSSLCertificateManager.GetClientCertificate
title: IMFSSLCertificateManager::GetClientCertificate
author: windows-sdk-content
description: Gets the client SSL certificate synchronously.
old-location: mf\imfsslcertificatemanager_getclientcertificate.htm
tech.root: medfound
ms.assetid: 11a575e8-5eb2-4cbb-a460-f1ea5d54d324
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetClientCertificate, GetClientCertificate method [Media Foundation], GetClientCertificate method [Media Foundation],IMFSSLCertificateManager interface, IMFSSLCertificateManager interface [Media Foundation],GetClientCertificate method, IMFSSLCertificateManager.GetClientCertificate, IMFSSLCertificateManager::GetClientCertificate, mf.imfsslcertificatemanager_getclientcertificate, mfidl/IMFSSLCertificateManager::GetClientCertificate
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
 - IMFSSLCertificateManager.GetClientCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSSLCertificateManager::GetClientCertificate


## -description


Gets the client SSL certificate synchronously.


## -parameters




### -param pszURL [in]

Pointer to a string that contains the URL for which a client-side SSL certificate is required. Media Foundation can resolve the scheme and send the request to the server.


### -param ppbData [out]

Pointer to the buffer that stores the certificate.
This caller must free the buffer by calling <b>CoTaskMemFree</b>.


### -param pcbData [out]

Pointer to a <b>DWORD</b> variable that receives the number of bytes required to hold the certificate data in the buffer pointed by <i>*ppbData</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62e4227d-6bc9-4011-acee-6278fe388830">IMFSSLCertificateManager</a>
 

 

