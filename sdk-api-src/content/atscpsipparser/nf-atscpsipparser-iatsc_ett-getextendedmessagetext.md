---
UID: NF:atscpsipparser.IATSC_ETT.GetExtendedMessageText
title: IATSC_ETT::GetExtendedMessageText method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_ett_getextendedmessagetext.htm
old-project: mstv
ms.assetid: 4e1b5f65-4662-41aa-8a11-cce6a2debb9e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetExtendedMessageText method [Microsoft TV Technologies], GetExtendedMessageText method [Microsoft TV Technologies], IATSC_ETT interface, GetExtendedMessageText,IATSC_ETT.GetExtendedMessageText, IATSC_ETT, IATSC_ETT interface [Microsoft TV Technologies], GetExtendedMessageText method, IATSC_ETT::GetExtendedMessageText, IATSC_ETTGetExtendedMessageText, atscpsipparser/IATSC_ETT::GetExtendedMessageText, mstv.iatsc_ett_getextendedmessagetext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: APPX_PACKAGE_WRITER_PAYLOAD_STREAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_ETT.GetExtendedMessageText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_ETT::GetExtendedMessageText method


## -description



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




<a href="https://msdn.microsoft.com/ae52e81e-4de1-480c-82bf-c9629064970c">IATSC_ETT Interface</a>
 

 

