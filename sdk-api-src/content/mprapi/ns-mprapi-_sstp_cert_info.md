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

# _SSTP_CERT_INFO structure


## -description


The <b>SSTP_CERT_INFO</b> structure  contains information about a Secure Socket Tunneling Protocool (SSTP) based certificate.


## -struct-fields




### -field isDefault

A value that is <b>TRUE</b> if this is the default mode, and <b>FALSE</b> otherwise.

<div class="alert"><b>Note</b>  Default mode is when the administrator has not explicitly configured the device and the SSTP service automatically chooses a valid certificate.</div>
<div> </div>

### -field certBlob

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure that contains the SSTP based certificate hash. 

The <b>cbData</b> member contains the length, in bytes, of the certificate hash in the <b>pbData</b> member. If <b>cbData</b> is zero, the SSTP certificate configuration is cleaned and the SSTP service automatically chooses a valid certificate. The hashing algorithm used to calculate <b>pbData</b> is defined by the <b>certAlgorithm</b> member of the <a href="https://msdn.microsoft.com/6f21d569-af9b-49ba-ab02-4dfc74e87ed2">SSTP_CONFIG_PARAMS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/19ad3493-99b7-405f-9663-3886388b5640">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>



<a href="https://msdn.microsoft.com/6f21d569-af9b-49ba-ab02-4dfc74e87ed2">SSTP_CONFIG_PARAMS</a>
 

 

