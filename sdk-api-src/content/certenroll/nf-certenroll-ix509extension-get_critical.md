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

# IX509Extension::get_Critical


## -description


The <b>Critical</b> property specifies and retrieves a Boolean value that identifies whether the certificate extension is critical. This property is web enabled on input.

This property is read/write.


## -parameters


## -remarks



A certificate extension consists of an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the extension value. The criticality indicates whether an application that uses a certificate can ignore the extension type and value. If an extension is identified as critical but the application does not recognize the extension type, the application should reject the certificate.




## -see-also




<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

