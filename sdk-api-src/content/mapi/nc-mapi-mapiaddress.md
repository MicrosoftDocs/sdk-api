---
UID: NC:mapi.MAPIADDRESS
title: MAPIADDRESS (mapi.h)
description: The MAPIAddress function creates or modifies a set of address list entries.
helpviewer_keywords: ["MAPIAddress","MAPIAddress callback","MAPIAddress callback function","MAPI_LOGON_UI","MAPI_NEW_SESSION","mapi.mapiaddress","mapi/MAPIAddress"]
old-location: mapi\mapiaddress.htm
tech.root: mapi
ms.assetid: 4f01763d-22a2-4ee4-a559-f875cb06ea6b
ms.date: 12/05/2018
ms.keywords: MAPIAddress, MAPIAddress callback, MAPIAddress callback function, MAPI_LOGON_UI, MAPI_NEW_SESSION, mapi.mapiaddress, mapi/MAPIAddress
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
 - MAPIADDRESS
 - mapi/MAPIADDRESS
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
 - MAPIAddress
---

# MAPIADDRESS callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIAddress</b> function creates or modifies a set of address list entries.

## -parameters

### -param lhSession [in]

Session handle that represents a Simple MAPI session or zero. If the value of the <i>lhSession</i> parameter is zero, MAPI logs on the user and creates a session that exists only for the duration of the call. This temporary session can be an existing shared session or a new one. If necessary, a logon dialog box is displayed.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i> ulUIParam</i> is ignored.

### -param lpszCaption [in]

Pointer to the caption for the address list dialog box, <b>NULL</b>, or an empty string. When the <i>lpszCaption</i> parameter is <b>NULL</b> or points to an empty string, <b>MAPIAddress</b> uses the default caption "Address Book."

### -param nEditFields [in]

The number of edit controls that should be present in the address list. The values 0 through 4 are valid. If the value of the <i>nEditFields</i> parameter is 4, each recipient class supported by the underlying messaging system has an edit control. If the value of <i>nEditFields</i> is zero, only address list browsing is possible. Values of 1, 2, or 3 control the number of edit controls present.  However, if the number of recipient classes in the array pointed to by the <i>lpRecips</i> parameter is greater than the value of <i>nEditFields</i>, the number of classes in <i>lpRecips</i> is used to indicate the number of edit controls instead of the value of <i>nEditFields</i>. If the value of <i>nEditFields</i> is 1 and more than one kind of entry exists in <i>lpRecips</i>, then the <i>lpszLabels</i> parameter is ignored. Entries selected for the different controls are differentiated by the <b>ulRecipClass</b> member in the returned recipient structure.

### -param lpszLabels [in]

Pointer to a string to be used as an edit control label in the address-list dialog box. When the <i>nEditFields</i> parameter is set to any value other than 1, the <i>lpszLabels</i> parameter is ignored and should be <b>NULL</b> or point to an empty string. Also, if the caller requires the default control label "To," <i>lpszLabels</i> should be <b>NULL</b> or point to an empty string.

### -param nRecips [in]

The number of entries in the array indicated by the <i>lpRecips</i> parameter.  If the value of the <i>nRecips</i> parameter is zero, <i>lpRecips</i> is ignored.

### -param lpRecips [in]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structures defining the initial recipient entries to be used to populate the address-list dialog box. The entries do not need to be grouped by recipient class; they are differentiated by the values of the <b>ulRecipClass</b> members of the <b>MapiRecipDesc</b> structures in the array. If the number of different recipient classes is greater than the value indicated by the <i>nEditFields</i> parameter, the <i>nEditFields</i> and <i>lpszLabels</i> parameters are ignored.

### -param flFlags [in]

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
An attempt should be made to create a new session rather than acquire the environment's shared session. If the MAPI_NEW_SESSION flag is not set, <b>MAPIAddress</b> uses an existing shared session.

</td>
</tr>
</table>

### -param ulReserved

Reserved; must be zero.

### -param lpnNewRecips [out]

Pointer to the number of entries in the <i>lppNewRecips</i> recipient output array. If the value of the <i>lpnNewRecips</i> parameter is zero, the <i>lppNewRecips</i> parameter is ignored.

### -param *lppNewRecips [out]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structures containing the final list of recipients. This array is allocated by <b>MAPIAddress</b>, cannot be <b>NULL</b>, and must be freed using <a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a>, even if there are no new recipients. Recipients are grouped by recipient class in the following order: MAPI_TO, MAPI_CC, MAPI_BCC.

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
One or more unspecified errors occurred while addressing the message. No list of recipient entries was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. No list of recipient entries was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_EDITFIELDS </b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>nEditFields</i> parameter was outside the range of 0 through 4. No list of recipient entries was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_RECIPS </b></dt>
</dl>
</td>
<td width="60%">
One or more of the recipients in the address list was not valid. No list of recipient entries was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was used for the <i>lhSession</i> parameter. No list of recipient entries was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. No list of recipient entries was returned.

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
The user canceled one of the dialog boxes. No list of recipient entries was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and a list of recipient entries was returned.

</td>
</tr>
</table>

## -remarks

The <b>MAPIAddress</b> function displays a standard address-list dialog box to show an initial set of zero or more recipients. The user can choose new entries to add to the set or make changes to existing entries. This dialog box cannot be suppressed, but the caller can set dialog box characteristics. The changed set of recipients is returned to the caller.

Before <b>MAPIAddress</b> writes new or changed recipient information, it must allocate memory for the structure array that will contain the information. Memory is also allocated as part of preloading the address book, regardless of whether new or changed recipient data is written. Client applications must call the <a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a> function to free this memory after <b>MAPIAddress</b> returns. If any error occurs, no memory was allocated and clients do not need to call <b>MAPIFreeBuffer</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>