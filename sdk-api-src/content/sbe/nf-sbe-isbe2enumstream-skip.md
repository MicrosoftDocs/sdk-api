---
UID: NF:sbe.ISBE2EnumStream.Skip
title: ISBE2EnumStream::Skip (sbe.h)
description: Skips a specified number of streams in the enumeration sequence.
helpviewer_keywords: ["ISBE2EnumStream interface [Microsoft TV Technologies]","Skip method","ISBE2EnumStream.Skip","ISBE2EnumStream::Skip","Skip","Skip method [Microsoft TV Technologies]","Skip method [Microsoft TV Technologies]","ISBE2EnumStream interface","mstv.isbe2enumstream_skip","sbe/ISBE2EnumStream::Skip"]
old-location: mstv\isbe2enumstream_skip.htm
tech.root: mstv
ms.assetid: 52979cbc-203b-49ae-9892-db1abfeae94b
ms.date: 12/05/2018
ms.keywords: ISBE2EnumStream interface [Microsoft TV Technologies],Skip method, ISBE2EnumStream.Skip, ISBE2EnumStream::Skip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],ISBE2EnumStream interface, mstv.isbe2enumstream_skip, sbe/ISBE2EnumStream::Skip
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows�7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sbe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISBE2EnumStream::Skip
 - sbe/ISBE2EnumStream::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2EnumStream.Skip
---

# ISBE2EnumStream::Skip


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Skips a specified number of streams in the enumeration sequence.

## -parameters

### -param cRecords [in]

The number of streams to skip.

## -returns

This method can return one of these values.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The end of the sequence was reached before skipping the requested number of streams.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a>