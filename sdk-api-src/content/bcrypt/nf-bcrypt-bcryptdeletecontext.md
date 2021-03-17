---
UID: NF:bcrypt.BCryptDeleteContext
title: BCryptDeleteContext function (bcrypt.h)
description: Deletes an existing CNG configuration context.
helpviewer_keywords: ["BCryptDeleteContext","BCryptDeleteContext function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","bcrypt/BCryptDeleteContext","security.bcryptdeletecontext"]
old-location: security\bcryptdeletecontext.htm
tech.root: security
ms.assetid: 6a250bed-0ea4-4cae-86e6-f0cea95dc56e
ms.date: 12/05/2018
ms.keywords: BCryptDeleteContext, BCryptDeleteContext function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, bcrypt/BCryptDeleteContext, security.bcryptdeletecontext
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
 - BCryptDeleteContext
 - bcrypt/BCryptDeleteContext
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
 - BCryptDeleteContext
---

# BCryptDeleteContext function


## -description

<p class="CCE_Message">[<b>BCryptDeleteContext</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>BCryptDeleteContext</b> function deletes an existing CNG configuration context.

## -parameters

### -param dwTable [in]

Identifies the configuration table to delete the context from. This can be one of the following values.

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
Delete the context from the local-machine configuration table.

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

A pointer to a null-terminated Unicode string that contains the identifier of the context to delete.

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
</table>

## -remarks

<b>BCryptDeleteContext</b> can be called only in user mode.

