---
UID: NF:bcrypt.BCryptQueryContextConfiguration
title: BCryptQueryContextConfiguration function (bcrypt.h)
description: Retrieves the current configuration for the specified CNG context.
helpviewer_keywords: ["BCryptQueryContextConfiguration","BCryptQueryContextConfiguration function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","bcrypt/BCryptQueryContextConfiguration","security.bcryptquerycontextconfiguration"]
old-location: security\bcryptquerycontextconfiguration.htm
tech.root: security
ms.assetid: 3e2ae471-cad6-4bfe-9e30-7b2a7014bc08
ms.date: 12/05/2018
ms.keywords: BCryptQueryContextConfiguration, BCryptQueryContextConfiguration function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, bcrypt/BCryptQueryContextConfiguration, security.bcryptquerycontextconfiguration
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptQueryContextConfiguration
 - bcrypt/BCryptQueryContextConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptQueryContextConfiguration
---

# BCryptQueryContextConfiguration function


## -description

<p class="CCE_Message">[<b>BCryptQueryContextConfiguration</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>BCryptQueryContextConfiguration</b> function retrieves the current configuration for the specified CNG context.

## -parameters

### -param dwTable [in]

Identifies the configuration table that the context exists in. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LOCAL"></a><a id="crypt_local"></a><dl>
<dt><b>CRYPT_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The context exists in the local-machine configuration table.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DOMAIN"></a><a id="crypt_domain"></a><dl>
<dt><b>CRYPT_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
This value is not available for use.

</td>
</tr>
</table>

### -param pszContext [in]

A pointer to a null-terminated Unicode string that contains the identifier of the context to obtain the configuration information for.

### -param pcbBuffer [in, out]

The address of a <b>ULONG</b> variable that, on entry, contains the size, in bytes, of the buffer pointed to by <i>ppBuffer</i>. If this size is not large enough to hold the context information, this function will fail with <b>STATUS_BUFFER_TOO_SMALL</b>.

After this function returns, this variable contains the number of bytes that were copied to the <i>ppBuffer</i> buffer.

### -param ppBuffer [in, out]

The address of a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_context_config">CRYPT_CONTEXT_CONFIG</a> structure that receives the context configuration information retrieved by this function. The value pointed to by the <i>pcbBuffer</i> parameter contains the size of this buffer.

If the value pointed to by this parameter is <b>NULL</b>, this function will allocate the required memory. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the variable pointed to by the <i>pcbBuffer</i> parameter and return <b>STATUS_BUFFER_TOO_SMALL</b>.

For more information on the usage of this parameter, see Remarks.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppBuffer</i> parameter is not <b>NULL</b>, and the value pointed to by the <i>pcbBuffer</i> parameter is not large enough to hold the set of contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified context could not be found.

</td>
</tr>
</table>

## -remarks

Each context has only one set of configuration information, so although the <i>ppBuffer</i> parameter appears to be a used as an array, this function treats this as an array with only one element. The following example helps clarify how this parameter is used.


```cpp
// Get the configuration information for the context.
CRYPT_CONTEXT_CONFIG config;
ULONG uSize = sizeof(config);
PCRYPT_CONTEXT_CONFIG pConfig = &config;
status = BCryptQueryContextConfiguration(
    CRYPT_LOCAL, 
    pszContextID, 
    &uSize, 
    &pConfig);

```


<b>BCryptQueryContextConfiguration</b> can be called only in user mode.