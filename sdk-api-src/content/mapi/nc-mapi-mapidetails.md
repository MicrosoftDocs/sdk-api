---
UID: NC:mapi.MAPIDETAILS
title: MAPIDETAILS (mapi.h)
description: The MAPIDetails function displays a dialog box containing the details of a selected address list entry.
helpviewer_keywords: ["MAPIDetails","MAPIDetails callback","MAPIDetails callback function","MAPI_AB_NOMODIFY","MAPI_LOGON_UI","MAPI_NEW_SESSION","mapi.mapidetails","mapi/MAPIDetails"]
old-location: mapi\mapidetails.htm
tech.root: mapi
ms.assetid: 28fbafff-8f34-4db8-bcb5-98f61883bea0
ms.date: 12/05/2018
ms.keywords: MAPIDetails, MAPIDetails callback, MAPIDetails callback function, MAPI_AB_NOMODIFY, MAPI_LOGON_UI, MAPI_NEW_SESSION, mapi.mapidetails, mapi/MAPIDetails
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
 - MAPIDETAILS
 - mapi/MAPIDETAILS
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
 - MAPIDetails
---

# MAPIDETAILS callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIDetails</b> function displays a dialog box containing the details of a selected address list entry.

## -parameters

### -param lhSession [in]

Session handle that represents a Simple MAPI session or zero. If the value of the <i>lhSession</i> parameter is zero, MAPI logs on the user and creates a session that exists only for the duration of the call. This temporary session can be an existing shared session or a new one. If additional information is required from the user to successfully complete the logon, a dialog box is displayed.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i> ulUIParam</i> is ignored.

### -param lpRecip [in]

Pointer to the recipient for which details are to be displayed.  <b>MAPIDetails</b> ignores all members of this <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structure except the <b>ulEIDSize</b> and <b>lpEntryID</b> members. If the value of <b>ulEIDSize</b> is nonzero, <b>MAPIDetails</b> resolves the recipient entry. If the value of <b>ulEIDSize</b> is zero, <b>MAPIDetails</b> returns the MAPI_E_AMBIGUOUS_RECIP value.

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
The caller is requesting that the dialog box be read-only, prohibiting changes. <b>MAPIDetails</b> might or might not honor the request.

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
An attempt should be made to create a new session rather than acquire the environment's shared session. If the MAPI_NEW_SESSION flag is not set, <b>MAPIDetails</b> uses an existing shared session.

</td>
</tr>
</table>

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
<dt><b>MAPI_E_AMBIGUOUS_RECIPIENT </b></dt>
</dl>
</td>
<td width="60%">
The dialog box could not be displayed because the <b>ulEIDSize</b> member of the structure pointed to by the <i>lpRecips</i> parameter was zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred. No dialog box was displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. No dialog box was displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_RECIPS </b></dt>
</dl>
</td>
<td width="60%">
The recipient specified in the <i>lpRecip</i> parameter was unknown or the recipient had an invalid <b>ulEIDSize</b> value. No dialog box was displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. No dialog box was displayed.

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
The user canceled either the logon dialog box or the details dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the details dialog box was displayed.

</td>
</tr>
</table>

## -remarks

The <b>MAPIDetails</b> function presents a dialog box that shows the details of a particular address list entry. The display name and address are the minimum attributes that are displayed in the dialog box; more information can be shown, depending on the address book provider. The details dialog box cannot be suppressed, but the caller can request that it be read-only or modifiable. 

Details can only be shown for resolved address list entries. An entry is resolved if the value of the <b>ulEIDSize</b> member of the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structure is nonzero. Entries are resolved when they are returned by the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiaddress">MAPIAddress</a> or <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiresolvename">MAPIResolveName</a> functions and as the result being recipients of read mail.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiaddress">MAPIAddress</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiresolvename">MAPIResolveName</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>