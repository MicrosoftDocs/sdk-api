---
UID: NC:mapi.MAPIRESOLVENAME
title: MAPIRESOLVENAME (mapi.h)
description: The MAPIResolveName function transforms a message recipient's name as entered by a user to an unambiguous address list entry.
helpviewer_keywords: ["MAPIResolveName","MAPIResolveName callback","MAPIResolveName callback function","MAPI_AB_NOMODIFY","MAPI_DIALOG","MAPI_LOGON_UI","MAPI_NEW_SESSION","mapi.mapiresolvename","mapi/MAPIResolveName"]
old-location: mapi\mapiresolvename.htm
tech.root: mapi
ms.assetid: c834ea40-62c6-44a8-b0e1-f569a92b4c83
ms.date: 12/05/2018
ms.keywords: MAPIResolveName, MAPIResolveName callback, MAPIResolveName callback function, MAPI_AB_NOMODIFY, MAPI_DIALOG, MAPI_LOGON_UI, MAPI_NEW_SESSION, mapi.mapiresolvename, mapi/MAPIResolveName
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
 - MAPIRESOLVENAME
 - mapi/MAPIRESOLVENAME
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
 - MAPIResolveName
---

# MAPIRESOLVENAME callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIResolveName</b> function transforms a message recipient's name as entered by a user to an unambiguous address list entry.

## -parameters

### -param lhSession [in]

Handle that represents a Simple MAPI session or zero. If the value of the <i>lhSession</i> parameter is zero, MAPI logs on the user and creates a session that exists only for the duration of the call. This temporary session can be an existing shared session or a new one. If necessary, the logon dialog box is displayed.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type <b>HWND</b> (cast to a <b>ULONG_PTR</b>). If no dialog box is displayed during the call, <i> ulUIParam</i> is ignored.

### -param lpszName [in]

Pointer to the name to be resolved.

### -param flFlags [in]

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_AB_NOMODIFY_"></a><a id="mapi_ab_nomodify_"></a><dl>
<dt><b>MAPI_AB_NOMODIFY </b></dt>
</dl>
</td>
<td width="60%">
The caller is requesting that the dialog box be read-only, prohibiting changes. <b>MAPIResolveName</b> ignores this flag if MAPI_DIALOG is not set. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_DIALOG_"></a><a id="mapi_dialog_"></a><dl>
<dt><b>MAPI_DIALOG </b></dt>
</dl>
</td>
<td width="60%">
A dialog box should be displayed for name resolution. If this flag is not set and the name cannot be resolved, <b>MAPIResolveName</b> returns the MAPI_E_AMBIGUOUS_RECIPIENT value.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_LOGON_UI_"></a><a id="mapi_logon_ui_"></a><dl>
<dt><b>MAPI_LOGON_UI </b></dt>
</dl>
</td>
<td width="60%">
A dialog box should be displayed to prompt the user to log on if required. When the MAPI_LOGON_UI flag is not set, the client application does not display a logon dialog box and returns an error value if the user is not logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_NEW_SESSION_"></a><a id="mapi_new_session_"></a><dl>
<dt><b>MAPI_NEW_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An attempt should be made to create a new session rather than acquire the environment's shared session. If the MAPI_NEW_SESSION flag is not set, <b>MAPIResolveName</b> uses an existing shared session.

</td>
</tr>
</table>

### -param ulReserved

Reserved; must be zero.

### -param *lppRecip [out]

Pointer to a recipient structure if the resolution results in a single match. The recipient structure contains the resolved name and related information. Memory for this structure must be freed using the <a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a> function.

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
<dt><b>MAPI_E_AMBIGUOUS_RECIPIENT </b></dt>
</dl>
</td>
<td width="60%">
The recipient requested has not been or could not be resolved to a unique address list entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_UNKNOWN_RECIPIENT </b></dt>
</dl>
</td>
<td width="60%">
The recipient could not be resolved to any address. The recipient might not exist or might be unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred. The name was not resolved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. The name was not resolved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. The name was not resolved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The operation was not supported by the underlying messaging system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_USER_ABORT </b></dt>
</dl>
</td>
<td width="60%">
The user canceled one of the dialog boxes. The name was not resolved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the name was resolved.

</td>
</tr>
</table>

## -remarks

The <b>MAPIResolveName</b> function resolves a message recipient's name (as entered by a user) to an unambiguous address list entry, optionally prompting the user to choose between possible entries, if necessary. A recipient descriptor structure containing fully resolved information about the entry is allocated and returned. The caller should free this <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structure at some point by calling the <a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a> function. If <b>MAPIResolveName</b> returns an error value, it is not necessary to deallocate memory with <b>MAPIFreeBuffer</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>