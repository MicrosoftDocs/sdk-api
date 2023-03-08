---
UID: NS:mapi.MapiRecipDescW
title: MapiRecipDescW (mapi.h)
description: A MapiRecipDescW structure contains information about a message sender or recipient.
helpviewer_keywords: ["*lpMapiRecipDescW","MAPI_BCC","MAPI_CC","MAPI_ORIG","MAPI_TO","MapiRecipDescW","MapiRecipDescW structure","lpMapiRecipDescW","lpMapiRecipDescW structure pointer","mapi.mapirecipdescw","mapi/MapiRecipDescW","mapi/lpMapiRecipDescW"]
old-location: mapi\mapirecipdescw.htm
tech.root: mapi
ms.assetid: 70050D1A-DA06-4D3B-90AF-F997E3B332EB
ms.date: 12/05/2018
ms.keywords: '*lpMapiRecipDescW, MAPI_BCC, MAPI_CC, MAPI_ORIG, MAPI_TO, MapiRecipDescW, MapiRecipDescW structure, lpMapiRecipDescW, lpMapiRecipDescW structure pointer, mapi.mapirecipdescw, mapi/MapiRecipDescW, mapi/lpMapiRecipDescW'
req.header: mapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MapiRecipDescW, *lpMapiRecipDescW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpMapiRecipDescW
 - mapi/lpMapiRecipDescW
 - MapiRecipDescW
 - mapi/MapiRecipDescW
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
 - MapiRecipDescW
---

# MapiRecipDescW structure


## -description

A <b>MapiRecipDescW</b> structure contains information about a message sender or recipient.

## -struct-fields

### -field ulReserved

Reserved; must be zero.

### -field ulRecipClass

Contains a numeric value that indicates the type of recipient. The following values are possible.

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
Indicates a primary recipient of the message.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_CC"></a><a id="mapi_cc"></a><dl>
<dt><b>MAPI_CC</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Indicates the recipient of a  copy of the message.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_BCC"></a><a id="mapi_bcc"></a><dl>
<dt><b>MAPI_BCC</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Indicates the recipient of a blind copy of the message.

</td>
</tr>
</table>

### -field lpszName

Pointer to the display name of the message recipient or sender.

### -field lpszAddress

Optional pointer to the recipient or sender's address.  This address contains provider-specific message delivery data.

Generally, the messaging system provides such addresses for inbound messages. For outbound messages, the <b>lpszAddress</b> member can point to an address entered by the user for a recipient that is not in an address book (a custom recipient).

The format of the address is <i>address type</i>:<i>email address</i>. Two examples of valid addresses are FAX:206-555-1212 and SMTP:M@X.COM.

### -field ulEIDSize

The size, in bytes, of the entry identifier pointed to by the <b>lpEntryID</b> member.

### -field lpEntryID

Pointer to an entry identifier that cannot be deciphered by client applications and that is used by a messaging system service provider to identify the message recipient.

These entry identifiers have meaning only for the service provider. The messaging system uses this member to return valid entry identifiers for all recipients or senders listed in the address book.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a>

