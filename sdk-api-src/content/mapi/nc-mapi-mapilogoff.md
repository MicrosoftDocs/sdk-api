---
UID: NC:mapi.MAPILOGOFF
title: MAPILOGOFF (mapi.h)
description: The MAPILogoff function ends a session with the messaging system.
helpviewer_keywords: ["MAPILogoff","MAPILogoff callback","MAPILogoff callback function","mapi.mapilogoff","mapi/MAPILogoff"]
old-location: mapi\mapilogoff.htm
tech.root: mapi
ms.assetid: d04316cf-31f5-4f5f-ad20-01ce720fdf4c
ms.date: 12/05/2018
ms.keywords: MAPILogoff, MAPILogoff callback, MAPILogoff callback function, mapi.mapilogoff, mapi/MAPILogoff
req.header: mapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAPILOGOFF
 - mapi/MAPILOGOFF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mapi.h
api_name:
 - MAPILogoff
---

# MAPILOGOFF callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPILogoff</b> function ends a session with the messaging system.

## -parameters

### -param lhSession [in]

Handle for the Simple MAPI session to be terminated. Session handles are returned by the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a> function and invalidated by <b>MAPILogoff</b>. The value of the <i>lhSession</i> parameter must represent a valid session; it cannot be zero.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.

### -param flFlags

Reserved; must be zero.

### -param ulReserved

Reserved; must be zero.

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
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
The <i>flFlags</i> parameter is invalid or one or more unspecified errors occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. The session was not terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was used for the <i>lhSession</i> parameter. The session was not terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the session was terminated.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>