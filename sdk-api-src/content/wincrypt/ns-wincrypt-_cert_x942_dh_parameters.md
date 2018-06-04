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

# _CERT_X942_DH_PARAMETERS structure


## -description


The <b>CERT_X942_DH_PARAMETERS</b> structure contains parameters associated with a Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a>.


## -struct-fields




### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.


### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).


### -field q

Prime Q. 




A factor of p–1. The most significant bit of the most significant byte must be set to 1.


### -field j

Optional subgroup factor.


### -field pValidationParams

Optional pointer to a <a href="https://msdn.microsoft.com/26c367d5-c338-4db3-9973-ce21dcddf7ca">CERT_X942_DH_VALIDATION_PARAMS</a> structure. If the <b>cbData</b> member of the q BLOB is zero, all of the members of <b>pValidationParams</b> must be zero.

