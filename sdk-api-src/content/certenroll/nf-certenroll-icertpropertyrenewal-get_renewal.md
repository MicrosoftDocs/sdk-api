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

# ICertPropertyRenewal::get_Renewal


## -description


The <b>Renewal</b> property retrieves the SHA-1 hash of the new certificate. The hash is returned in a byte array , and the byte array is represented by a Unicode encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method or the <a href="https://msdn.microsoft.com/87e0eabf-7a4a-4ff2-a9ce-6482f119cafd">InitializeFromCertificateHash</a> method to specify a value for the <b>Renewal</b> property.




## -see-also




<a href="https://msdn.microsoft.com/c87a391a-aec9-4b42-8084-c593ecbb0bc6">ICertPropertyRenewal</a>
 

 

