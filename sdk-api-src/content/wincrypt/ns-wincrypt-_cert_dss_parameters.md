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

# _CERT_DSS_PARAMETERS structure


## -description


The <b>CERT_DSS_PARAMETERS</b> structure contains parameters associated with a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Standard</a> (DSS) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> algorithm.


## -struct-fields




### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.


### -field q

Prime Q. It is 20 bytes in length. The most significant bit of the most significant byte must be set to 1.


### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).

