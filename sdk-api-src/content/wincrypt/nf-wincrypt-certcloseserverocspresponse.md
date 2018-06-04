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

# CertCloseServerOcspResponse function


## -description


The <b>CertCloseServerOcspResponse</b> function closes an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) server response handle.


## -parameters




### -param hServerOcspResponse [in]

The handle to close for an OCSP server response.


### -param dwFlags [in]

This parameter is not used and must be zero.


## -returns



This function does not return a value.




## -remarks



The <b>CertCloseServerOcspResponse</b> function closes a handle returned by either the <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a> or <a href="https://msdn.microsoft.com/6ccc0e85-1fa0-480c-a5b4-b21ba811e5d0">CertAddRefServerOcspResponse</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a>
 

 

