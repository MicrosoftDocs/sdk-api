---
UID: NS:mapi.MapiRecipDesc
title: MapiRecipDesc (mapi.h)
description: A MapiRecipDesc structure contains information about a message sender or recipient. For Unicode support, use the MapiRecipDescW structure.
helpviewer_keywords: ["*lpMapiRecipDesc","MAPI_BCC","MAPI_CC","MAPI_ORIG","MAPI_TO","MapiRecipDesc","MapiRecipDesc structure","lpMapiRecipDesc","lpMapiRecipDesc structure pointer","mapi.mapirecipdesc","mapi/MapiRecipDesc","mapi/lpMapiRecipDesc"]
old-location: mapi\mapirecipdesc.htm
tech.root: mapi
ms.assetid: 1457617f-de55-4875-91f5-afddee84b782
ms.date: 12/05/2018
ms.keywords: '*lpMapiRecipDesc, MAPI_BCC, MAPI_CC, MAPI_ORIG, MAPI_TO, MapiRecipDesc, MapiRecipDesc structure, lpMapiRecipDesc, lpMapiRecipDesc structure pointer, mapi.mapirecipdesc, mapi/MapiRecipDesc, mapi/lpMapiRecipDesc'
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
req.typenames: MapiRecipDesc, *lpMapiRecipDesc
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpMapiRecipDesc
 - mapi/lpMapiRecipDesc
 - MapiRecipDesc
 - mapi/MapiRecipDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiRecipDesc
---

# MapiRecipDesc structure


## -description

A <b>MapiRecipDesc</b> structure contains information about a message sender or recipient. For Unicode support, use the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdescw">MapiRecipDescW</a> structure.

## -struct-fields

### -field ulReserved

Reserved; must be zero.

### -field ulRecipClass

Contains a numeric value that indicates the type of recipient. Possible values are as follow.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_ORIG"></a><a id="mapi_orig"></a><dl>
<dt><b>MAPI_ORIG</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Indicates the original sender of the message. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_TO"></a><a id="mapi_to"></a><dl>
<dt><b>MAPI_TO</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Indicates a primary message recipient. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_CC"></a><a id="mapi_cc"></a><dl>
<dt><b>MAPI_CC</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Indicates a recipient of a message copy. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_BCC"></a><a id="mapi_bcc"></a><dl>
<dt><b>MAPI_BCC</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Indicates a recipient of a blind copy. 

</td>
</tr>
</table>

### -field lpszName

Pointer to the display name of the message recipient or sender.

### -field lpszAddress

Optional pointer to the recipient or sender's address; this address is provider-specific message delivery data. Generally, the messaging system provides such addresses for inbound messages. For outbound messages, the <b>lpszAddress</b> member can point to an address entered by the user for a recipient not in an address book (that is, a custom recipient).

The format of the address is <i>address type</i>:<i>email address</i>. Examples of valid addresses are FAX:206-555-1212 and SMTP:M@X.COM.

### -field ulEIDSize

The size, in bytes, of the entry identifier pointed to by the <b>lpEntryID</b> member.

### -field lpEntryID

Pointer to an opaque entry identifier used by a messaging system service provider to identify the message recipient. Entry identifiers have meaning only for the service provider; client applications will not be able to decipher them. The messaging system uses this member to return valid entry identifiers for all recipients or senders listed in the address book.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiaddress">MAPIAddress</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapidetails">MAPIDetails</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiresolvename">MAPIResolveName</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdescw">MapiRecipDescW</a>

