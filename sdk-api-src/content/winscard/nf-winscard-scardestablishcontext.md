---
UID: NF:winscard.SCardEstablishContext
title: SCardEstablishContext function (winscard.h)
description: Establishes the resource manager context (the scope) within which database operations are performed.
helpviewer_keywords: ["SCARD_SCOPE_SYSTEM","SCARD_SCOPE_USER","SCardEstablishContext","SCardEstablishContext function [Security]","_smart_scardestablishcontext","security.scardestablishcontext","winscard/SCardEstablishContext"]
old-location: security\scardestablishcontext.htm
tech.root: security
ms.assetid: 1cf9b005-b76c-4fc9-b4bd-a1ad8552535f
ms.date: 12/05/2018
ms.keywords: SCARD_SCOPE_SYSTEM, SCARD_SCOPE_USER, SCardEstablishContext, SCardEstablishContext function [Security], _smart_scardestablishcontext, security.scardestablishcontext, winscard/SCardEstablishContext
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardEstablishContext
 - winscard/SCardEstablishContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-winscard-l1-1-1.dll
 - Winscard.dll
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardEstablishContext
---

# SCardEstablishContext function


## -description

The <b>SCardEstablishContext</b> function establishes the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> (the scope) within which database operations are performed.

## -parameters

### -param dwScope [in]

Scope of the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_SCOPE_USER"></a><a id="scard_scope_user"></a><dl>
<dt><b>SCARD_SCOPE_USER</b></dt>
</dl>
</td>
<td width="60%">
Database operations are performed within the domain of the user.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SCOPE_SYSTEM"></a><a id="scard_scope_system"></a><dl>
<dt><b>SCARD_SCOPE_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
Database operations are performed within the domain of the system. The calling application must have appropriate access permissions for any database actions.

</td>
</tr>
</table>

### -param pvReserved1 [in]

Reserved for future use and must be <b>NULL</b>. This parameter will allow a suitably privileged management application to act on behalf of another user.

### -param pvReserved2 [in]

Reserved for future use and must be <b>NULL</b>.

### -param phContext [out]

A handle to the established <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. This handle can now be supplied to other functions attempting to do work within this context.

## -returns

If the function succeeds, the function returns SCARD_S_SUCCESS. 

If the function fails, it returns an error code. For more information, see <a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

## -remarks

The context handle returned by <b>SCardEstablishContext</b> can be used by database query and management functions. For more information, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a> and 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.

To release an established resource manager context, use 
<a href="/windows/desktop/api/winscard/nf-winscard-scardreleasecontext">SCardReleaseContext</a>.

If the client attempts a smart card operation in a remote session, such as a client session running on a terminal server, and the operating system in use does not support smart card redirection, this function returns ERROR_BROKEN_PIPE.


#### Examples

The following example establishes a resource manager context.


```cpp
SCARDCONTEXT    hSC;
LONG            lReturn;
// Establish the context.
lReturn = SCardEstablishContext(SCARD_SCOPE_USER,
                                NULL,
                                NULL,
                                &hSC);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardEstablishContext\n");
else
{
    // Use the context as needed. When done,
    // free the context by calling SCardReleaseContext.
    // ...
}

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardreleasecontext">SCardReleaseContext</a>