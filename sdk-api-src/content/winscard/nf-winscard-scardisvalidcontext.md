---
UID: NF:winscard.SCardIsValidContext
title: SCardIsValidContext function (winscard.h)
description: Determines whether a smart card context handle is valid.
helpviewer_keywords: ["SCardIsValidContext","SCardIsValidContext function [Security]","_smart_scardisvalidcontext","security.scardisvalidcontext","winscard/SCardIsValidContext"]
old-location: security\scardisvalidcontext.htm
tech.root: security
ms.assetid: 50bcb6aa-6265-4035-8265-45990f791ce3
ms.date: 12/05/2018
ms.keywords: SCardIsValidContext, SCardIsValidContext function [Security], _smart_scardisvalidcontext, security.scardisvalidcontext, winscard/SCardIsValidContext
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
 - SCardIsValidContext
 - winscard/SCardIsValidContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardIsValidContext
---

# SCardIsValidContext function


## -description

The <b>SCardIsValidContext</b> function determines whether a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> context handle is valid.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context can be set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_S_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The <i>hContext</i> parameter is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hContext</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other values</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

Call this function to determine whether a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> context handle is still valid. After a smart card context handle has been set by 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>, it may become not valid if the <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> service has been shut down.


#### Examples

The following example  shows determining whether a smart card context handle is valid.


```cpp
// Check the smart card context handle.
// hContext was set previously by SCardEstablishContext.

LONG    lReturn;
lReturn = SCardIsValidContext(hContext);
if ( SCARD_S_SUCCESS != lReturn )
{
    // Function failed; check return value.
    if ( ERROR_INVALID_HANDLE == lReturn )
        printf("Handle is invalid\n");
    else
    {
        // Some unexpected error occurred; report and bail out.
        printf("Failed SCardIsValidContext - %x\n", lReturn);
        exit(1);  // Or other appropriate error action.
    }
}
else
{
    // Handle is valid; proceed as needed.
    // ...
}

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>