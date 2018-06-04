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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62e4227d-6bc9-4011-acee-6278fe388830">IMFSSLCertificateManager</a>
 

 

