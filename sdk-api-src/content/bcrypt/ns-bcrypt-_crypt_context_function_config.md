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

# _CRYPT_CONTEXT_FUNCTION_CONFIG structure


## -description


The <b>CRYPT_CONTEXT_FUNCTION_CONFIG</b> structure contains configuration information for a cryptographic function of a CNG context.


## -struct-fields




### -field dwFlags

A set of flags that determine the options for the context function configuration. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXCLUSIVE"></a><a id="crypt_exclusive"></a><dl>
<dt><b>CRYPT_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
Restricts the set of usable providers for this function to only those that this function is specifically registered to support.

</td>
</tr>
</table>
 


### -field dwReserved

 




## -see-also




<a href="https://msdn.microsoft.com/e93c5e3e-3c63-49a3-8c8c-6510e10611ea">BCryptConfigureContextFunction</a>
 

 

