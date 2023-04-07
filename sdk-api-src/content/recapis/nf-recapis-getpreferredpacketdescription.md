---
UID: NF:recapis.GetPreferredPacketDescription
title: GetPreferredPacketDescription function (recapis.h)
description: Retrieves a packet description that contains the packet properties the recognizer uses.
helpviewer_keywords: ["6600b345-db7a-49ca-a54a-7d212952cb8f","GetPreferredPacketDescription","GetPreferredPacketDescription function [Tablet PC]","recapis/GetPreferredPacketDescription","tablet.getpreferredpacketdescription"]
old-location: tablet\getpreferredpacketdescription.htm
tech.root: tablet
ms.assetid: 6600b345-db7a-49ca-a54a-7d212952cb8f
ms.date: 12/05/2018
ms.keywords: 6600b345-db7a-49ca-a54a-7d212952cb8f, GetPreferredPacketDescription, GetPreferredPacketDescription function [Tablet PC], recapis/GetPreferredPacketDescription, tablet.getpreferredpacketdescription
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPreferredPacketDescription
 - recapis/GetPreferredPacketDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetPreferredPacketDescription
---

# GetPreferredPacketDescription function


## -description

Retrieves a packet description that contains the packet properties the recognizer uses.

## -parameters

### -param hrec

Handle to the recognizer.

### -param pPacketDescription

Describes the content of the packets the recognizer uses. For more information, see the <a href="/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description">PACKET_DESCRIPTION</a> structure.

To retrieve the packet description, initialize the packet description with zeroes and call the <b>GetPreferredPacketDescription</b> function. The function populates the property and button counts, which you use to allocate space for the pPacketProperties and pguidButtons members of the <a href="/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description">PACKET_DESCRIPTION</a> structure. Call the function again to populate the rest of the packet description.

The pguidButtons member of the <a href="/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description">PACKET_DESCRIPTION</a> structure may be zero when <b>GetPreferredPacketDescription</b> returns. This means the packets have no button data, so this member does not have any pguidButtons allocated. In this case, the calling function should leave the pointer <b>NULL</b>.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPacketDescription</i> buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>

## -remarks

Typically, recognizers use the (x, y) coordinate properties and ignore the others. If you save the ink to a file for recognition at a later time, use the preferred packet description to only save those properties that the recognizer uses.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-addstroke">AddStroke Function</a>



<a href="/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description">PACKET_DESCRIPTION Structure</a>