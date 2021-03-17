---
UID: NS:bcrypt._CRYPT_CONTEXT_CONFIG
title: CRYPT_CONTEXT_CONFIG (bcrypt.h)
description: Contains configuration information for a CNG context.
helpviewer_keywords: ["*PCRYPT_CONTEXT_CONFIG","CRYPT_CONTEXT_CONFIG","CRYPT_CONTEXT_CONFIG structure [Security]","CRYPT_EXCLUSIVE","CRYPT_OVERRIDE","PCRYPT_CONTEXT_CONFIG","PCRYPT_CONTEXT_CONFIG structure pointer [Security]","bcrypt/CRYPT_CONTEXT_CONFIG","bcrypt/PCRYPT_CONTEXT_CONFIG","security.crypt_context_config"]
old-location: security\crypt_context_config.htm
tech.root: security
ms.assetid: 3e07b7ae-84ef-4b77-bd49-d96906eaa4f8
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CONTEXT_CONFIG, CRYPT_CONTEXT_CONFIG, CRYPT_CONTEXT_CONFIG structure [Security], CRYPT_EXCLUSIVE, CRYPT_OVERRIDE, PCRYPT_CONTEXT_CONFIG, PCRYPT_CONTEXT_CONFIG structure pointer [Security], bcrypt/CRYPT_CONTEXT_CONFIG, bcrypt/PCRYPT_CONTEXT_CONFIG, security.crypt_context_config'
req.header: bcrypt.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_CONTEXT_CONFIG, *PCRYPT_CONTEXT_CONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CONTEXT_CONFIG
 - bcrypt/_CRYPT_CONTEXT_CONFIG
 - PCRYPT_CONTEXT_CONFIG
 - bcrypt/PCRYPT_CONTEXT_CONFIG
 - CRYPT_CONTEXT_CONFIG
 - bcrypt/CRYPT_CONTEXT_CONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - CRYPT_CONTEXT_CONFIG
---

# CRYPT_CONTEXT_CONFIG structure


## -description

The <b>CRYPT_CONTEXT_CONFIG</b> structure contains configuration information for a CNG context.

## -struct-fields

### -field dwFlags

A set of flags that determine the options for the configuration context. This can be zero or a combination of one or more of the following values.

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
Restricts the set of cryptographic functions in an interface to those that the current CNG  context is specifically registered to support. 

If this flag is set, then any attempts to resolve a given function will succeed only if one of the following is true:

<ul>
<li>The function exists within the current CNG context.</li>
<li>The function exists in some interface in the default context, and an instance of that same interface also exists within the current CNG context.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OVERRIDE"></a><a id="crypt_override"></a><dl>
<dt><b>CRYPT_OVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this entry in the enterprise-wide configuration table should take precedence over any and all corresponding entries in the local-machine configuration table for this context. This flag only applies to entries in the enterprise-wide configuration table. Without this flag, local machine configuration entries take precedence.

</td>
</tr>
</table>

### -field dwReserved

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptconfigurecontext">BCryptConfigureContext</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatecontext">BCryptCreateContext</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptquerycontextconfiguration">BCryptQueryContextConfiguration</a>