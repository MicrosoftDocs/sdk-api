---
UID: NF:mfidl.IMFSSLCertificateManager.OnServerCertificate
title: IMFSSLCertificateManager::OnServerCertificate method
author: windows-driver-content
description: Called by Media Foundation when the server SSL certificate has been received; indicates whether the server certificate is accepted.
old-location: mf\imfsslcertificatemanager_onservercertificate.htm
old-project: medfound
ms.assetid: 4ba43175-4429-437d-acfb-e0ea8d300651
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMFSSLCertificateManager, IMFSSLCertificateManager interface [Media Foundation], OnServerCertificate method, IMFSSLCertificateManager::OnServerCertificate, OnServerCertificate method [Media Foundation], OnServerCertificate method [Media Foundation], IMFSSLCertificateManager interface, OnServerCertificate,IMFSSLCertificateManager.OnServerCertificate, mf.imfsslcertificatemanager_onservercertificate, mfidl/IMFSSLCertificateManager::OnServerCertificate
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFSSLCertificateManager.OnServerCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSSLCertificateManager::OnServerCertificate method


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62e4227d-6bc9-4011-acee-6278fe388830">IMFSSLCertificateManager</a>
 

 

