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

# _CRYPT_SMIME_CAPABILITIES structure


## -description


The <b>CRYPT_SMIME_CAPABILITIES</b> structure contains a prioritized array of supported capabilities. Capabilities include signature algorithms, <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric algorithms</a>, key enciphering algorithms, and non-algorithm capabilities, which are the preference for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signed data</a> and the preference for unencrypted messages.
<div class="alert"><b>Note</b>  The <b>CRYPT_SMIME_CAPABILITIES</b> are part of an Internet draft proposal. For a complete definition, see "draft-dusse-s/mime-cert-01.txt" dated May 5, 1997.</div><div> </div>

## -struct-fields




### -field cCapability

Count of elements in the <b>rgCapability</b> array.


### -field rgCapability

Prioritized array of pointers to 
<a href="https://msdn.microsoft.com/c7d1e04f-d2b9-4bab-88f4-8a528c527e7c">CRYPT_SMIME_CAPABILITY</a> structures each indicating a capability or preference of a user.


## -see-also




<a href="https://msdn.microsoft.com/c7d1e04f-d2b9-4bab-88f4-8a528c527e7c">CRYPT_SMIME_CAPABILITY</a>
 

 

