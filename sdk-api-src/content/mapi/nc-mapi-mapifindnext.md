---
UID: NC:mapi.MAPIFINDNEXT
title: MAPIFINDNEXT (mapi.h)
description: The MAPIFindNext function retrieves the next (or first) message identifier of a specified type of incoming message.
helpviewer_keywords: ["MAPIFindNext","MAPIFindNext callback","MAPIFindNext callback function","MAPI_GUARANTEE_FIFO","MAPI_LONG_MSGID","MAPI_UNREAD_ONLY","mapi.mapifindnext","mapi/MAPIFindNext"]
old-location: mapi\mapifindnext.htm
tech.root: mapi
ms.assetid: 6c11e88c-2883-4486-9679-2bdf0b30b8b0
ms.date: 12/05/2018
ms.keywords: MAPIFindNext, MAPIFindNext callback, MAPIFindNext callback function, MAPI_GUARANTEE_FIFO, MAPI_LONG_MSGID, MAPI_UNREAD_ONLY, mapi.mapifindnext, mapi/MAPIFindNext
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
 - MAPIFINDNEXT
 - mapi/MAPIFINDNEXT
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
 - MAPIFindNext
---

# MAPIFINDNEXT callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIFindNext</b> function retrieves the next (or first) message identifier of a specified type of incoming message.

## -parameters

### -param lhSession [in]

Session handle that represents a Simple MAPI session. The value of the <i>lhSession</i> parameter must represent a valid session; it cannot be zero.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.

### -param lpszMessageType [in]

Pointer to a string identifying the message class to search. To find an interpersonal message (IPM), specify <b>NULL</b> in the <i>lpszMessageType</i> parameter or have it point to an empty string. Messaging systems whose only supported message class is IPM can ignore this parameter.

### -param lpszSeedMessageID [in]

Pointer to a string containing the message identifier seed for the request. If the <i>lpszSeedMessageID</i> parameter is <b>NULL</b> or points to an empty string, <b>MAPIFindNext</b> retrieves the first message that matches the type specified in the <i>lpszMessageType</i> parameter.

### -param flFlags [in]

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_GUARANTEE_FIFO_"></a><a id="mapi_guarantee_fifo_"></a><dl>
<dt><b>MAPI_GUARANTEE_FIFO </b></dt>
</dl>
</td>
<td width="60%">
The message identifiers returned should be in the order of time received. <b>MAPIFindNext</b> calls can take longer if this flag is set. Some implementations cannot honor this request and return the MAPI_E_NO_SUPPORT value.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_LONG_MSGID_"></a><a id="mapi_long_msgid_"></a><dl>
<dt><b>MAPI_LONG_MSGID </b></dt>
</dl>
</td>
<td width="60%">
The returned message identifier can be as long as 512 characters. If this flag is set, the <i>lpszMessageID</i> parameter must be large enough to accommodate 512 characters.

Older versions of MAPI supported smaller message identifiers (64 bytes) and did not include this flag. <b>MAPIFindNext</b> will succeed without this flag set as long as <i>lpszMessageID</i> is large enough to hold the message identifier. If <i>lpszMessageID</i> cannot hold the message identifier, <b>MAPIFindNext</b> will fail.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_UNREAD_ONLY_"></a><a id="mapi_unread_only_"></a><dl>
<dt><b>MAPI_UNREAD_ONLY </b></dt>
</dl>
</td>
<td width="60%">
Only unread messages of the specified type should be enumerated. If this flag is not set, <b>MAPIFindNext</b> can return any message of the specified type.

</td>
</tr>
</table>

### -param ulReserved

Reserved; must be zero.

### -param lpszMessageID [out]

Pointer to the returned message identifier. The caller is responsible for allocating the memory. To ensure compatibility, allocate 512 characters and set MAPI_LONG_MSGID in the <i>flFlags</i> parameter. A smaller buffer is sufficient only if the returned message identifier is always 64 characters or less.

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
One or more unspecified errors occurred while matching the message type. The call failed before message type matching could take place.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. No message was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_MESSAGE </b></dt>
</dl>
</td>
<td width="60%">
An invalid message identifier was passed in the <i>lpszSeedMessageID</i> parameter. No message was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was passed in the <i>lhSession</i> parameter. No message was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_NO_MESSAGES </b></dt>
</dl>
</td>
<td width="60%">
A matching message could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the message identifier was returned.

</td>
</tr>
</table>

## -remarks

The <b>MAPIFindNext</b> function allows a client application to enumerate messages of a given type. This function can be called repeatedly to list all messages in the folder. Message identifiers returned from <b>MAPIFindNext</b> can be used in other Simple MAPI calls to retrieve message contents and delete messages. This function is for processing incoming messages, not for managing received messages. 

<b>MAPIFindNext</b> looks for messages in the folder in which new messages of the specified type are delivered. <b>MAPIFindNext</b> calls can be made only in the context of a valid Simple MAPI session established with the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a> function.

When the <i>lpszSeedMessageID</i> parameter is <b>NULL</b> or points to an empty string, <b>MAPIFindNext</b> returns the message identifier for the first message of the type specified by the <i>lpszMessageType</i> parameter. When <i>lpszSeedMessageID</i> contains a valid identifier, the function returns the next matching message of the type specified by <i>lpszMessageType</i>. Repeated calls to <b>MAPIFindNext</b> ultimately result in a return of the MAPI_E_NO_MESSAGES value, which means the enumeration is complete. 

Message type matching is done against message class strings. All message types whose names match (up to the length specified in <i>lpszMessageType</i>) are returned. 

Because message identifiers are messaging system-specific and can be invalidated at any time, message identifiers are valid only for the current session. If the message identifier passed in <i>lpszSeedMessageID</i> is invalid, <b>MAPIFindNext</b> returns the MAPI_E_INVALID_MESSAGE value.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>