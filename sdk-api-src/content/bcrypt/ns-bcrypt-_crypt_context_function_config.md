---
UID: NS:bcrypt._CRYPT_CONTEXT_FUNCTION_CONFIG
title: "_CRYPT_CONTEXT_FUNCTION_CONFIG"
author: windows-sdk-content
description: Contains configuration information for a cryptographic function of a CNG context.
old-location: security\crypt_context_function_config.htm
old-project: seccng
ms.assetid: 53026095-c871-4027-ac7d-428f1cb4aafe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCRYPT_CONTEXT_FUNCTION_CONFIG, CRYPT_CONTEXT_FUNCTION_CONFIG, CRYPT_CONTEXT_FUNCTION_CONFIG structure [Security], CRYPT_EXCLUSIVE, PCRYPT_CONTEXT_FUNCTION_CONFIG, PCRYPT_CONTEXT_FUNCTION_CONFIG structure pointer [Security], _CRYPT_CONTEXT_FUNCTION_CONFIG, bcrypt/CRYPT_CONTEXT_FUNCTION_CONFIG, bcrypt/PCRYPT_CONTEXT_FUNCTION_CONFIG, security.crypt_context_function_config"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bcrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRYPT_CONTEXT_FUNCTION_CONFIG, *PCRYPT_CONTEXT_FUNCTION_CONFIG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - CRYPT_CONTEXT_FUNCTION_CONFIG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

