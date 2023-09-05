---
UID: NF:atscpsipparser.IATSC_ETT.GetExtendedMessageText
title: IATSC_ETT::GetExtendedMessageText (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetExtendedMessageText","GetExtendedMessageText method [Microsoft TV Technologies]","GetExtendedMessageText method [Microsoft TV Technologies]","IATSC_ETT interface","IATSC_ETT interface [Microsoft TV Technologies]","GetExtendedMessageText method","IATSC_ETT.GetExtendedMessageText","IATSC_ETT::GetExtendedMessageText","IATSC_ETTGetExtendedMessageText","atscpsipparser/IATSC_ETT::GetExtendedMessageText","mstv.iatsc_ett_getextendedmessagetext"]
old-location: mstv\iatsc_ett_getextendedmessagetext.htm
tech.root: mstv
ms.assetid: 4e1b5f65-4662-41aa-8a11-cce6a2debb9e
ms.date: 12/05/2018
ms.keywords: GetExtendedMessageText, GetExtendedMessageText method [Microsoft TV Technologies], GetExtendedMessageText method [Microsoft TV Technologies],IATSC_ETT interface, IATSC_ETT interface [Microsoft TV Technologies],GetExtendedMessageText method, IATSC_ETT.GetExtendedMessageText, IATSC_ETT::GetExtendedMessageText, IATSC_ETTGetExtendedMessageText, atscpsipparser/IATSC_ETT::GetExtendedMessageText, mstv.iatsc_ett_getextendedmessagetext
req.header: atscpsipparser.h
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
 - IATSC_ETT::GetExtendedMessageText
 - atscpsipparser/IATSC_ETT::GetExtendedMessageText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_ETT.GetExtendedMessageText
---

# IATSC_ETT::GetExtendedMessageText


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetExtendedMessageText</b> method returns the message text.

## -parameters

### -param pdwLength [out]

Receives the length of the title text, in bytes.

### -param ppText [out]

Receives a pointer to the title text buffer. The method allocates the buffer and fills it with the title text, which is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65. The caller must free the buffer by calling <b>CoTaskMemFree</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The length of the text is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_ett">IATSC_ETT Interface</a>