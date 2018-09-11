---
UID: NS:mapi.MapiRecipDesc
title: MapiRecipDesc
author: windows-sdk-content
description: A MapiRecipDesc structure contains information about a message sender or recipient. For Unicode support, use the MapiRecipDescW structure.
old-location: mapi\mapirecipdesc.htm
tech.root: WindowsMAPI
ms.assetid: 1457617f-de55-4875-91f5-afddee84b782
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*lpMapiRecipDesc, MAPI_BCC, MAPI_CC, MAPI_ORIG, MAPI_TO, MapiRecipDesc, MapiRecipDesc structure, lpMapiRecipDesc, lpMapiRecipDesc structure pointer, mapi.mapirecipdesc, mapi/MapiRecipDesc, mapi/lpMapiRecipDesc"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiRecipDesc
product: Windows
targetos: Windows
req.typenames: MapiRecipDesc, *lpMapiRecipDesc
req.redist: 
---

# MapiRecipDesc structure


## -description


A <b>MapiRecipDesc</b> structure contains information about a message sender or recipient. For Unicode support, use the <a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">MapiRecipDescW</a> structure.


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




<a href="https://msdn.microsoft.com/4f01763d-22a2-4ee4-a559-f875cb06ea6b">MAPIAddress</a>



<a href="https://msdn.microsoft.com/28fbafff-8f34-4db8-bcb5-98f61883bea0">MAPIDetails</a>



<a href="https://msdn.microsoft.com/c834ea40-62c6-44a8-b0e1-f569a92b4c83">MAPIResolveName</a>



<a href="https://msdn.microsoft.com/7f696dd6-bfae-4c7d-b55f-d37952691c02">MapiMessage</a>



<a href="https://msdn.microsoft.com/3C74A9C0-1483-4A97-94EB-19A0D30D9A08">MapiMessageW</a>



<a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">MapiRecipDescW</a>
 

 

