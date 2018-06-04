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

# CertAddRefServerOcspResponse function


## -description


The <b>CertAddRefServerOcspResponse</b> function increments the reference count for an <b>HCERT_SERVER_OCSP_RESPONSE</b> handle.


## -parameters




### -param hServerOcspResponse [in]

A handle to an <b>HCERT_SERVER_OCSP_RESPONSE</b> returned by <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a>.


## -returns



This function has no return value.




## -remarks



Each <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a> and <b>CertAddRefServerOcspResponse</b> requires a corresponding <a href="https://msdn.microsoft.com/6247e8ca-ba12-432f-9bf8-a6c644f253e9">CertCloseServerOcspResponse</a>.



