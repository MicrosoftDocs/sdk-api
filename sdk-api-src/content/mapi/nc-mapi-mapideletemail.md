---
UID: NC:mapi.MAPIDELETEMAIL
title: MAPIDELETEMAIL (mapi.h)
description: The MAPIDeleteMail function deletes a message.
helpviewer_keywords: ["MAPIDeleteMail","MAPIDeleteMail callback","MAPIDeleteMail callback function","mapi.mapideletemail","mapi/MAPIDeleteMail"]
old-location: mapi\mapideletemail.htm
tech.root: mapi
ms.assetid: b149ef88-de0e-4a99-9150-7250d2b9540a
ms.date: 12/05/2018
ms.keywords: MAPIDeleteMail, MAPIDeleteMail callback, MAPIDeleteMail callback function, mapi.mapideletemail, mapi/MAPIDeleteMail
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
 - MAPIDELETEMAIL
 - mapi/MAPIDELETEMAIL
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
 - MAPIDeleteMail
---

# MAPIDELETEMAIL callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIDeleteMail</b> function deletes a message.

## -parameters

### -param lhSession [in]

Session handle that represents a valid Simple MAPI session. The value of the <i>lhSession</i> parameter must represent a valid session; it cannot be zero.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i> ulUIParam</i> is ignored.

### -param lpszMessageID [in]

The identifier for the message to be deleted. This identifier is messaging system-specific and will be invalid when <b>MAPIDeleteMail</b> successfully returns.

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
One or more unspecified errors occurred while deleting the message. No message was deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. No message was deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_MESSAGE </b></dt>
</dl>
</td>
<td width="60%">
An invalid message identifier was passed in the <i>lpszMessageID</i> parameter. No message was deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was passed in the <i>lhSession</i> parameter. No message was deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the message was deleted.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapifindnext">MAPIFindNext</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisavemail">MAPISaveMail</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>