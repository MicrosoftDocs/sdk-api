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
 

 

