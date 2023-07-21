---
UID: NF:atscpsipparser.IATSC_STT.GetCountOfTableDescriptors
title: IATSC_STT::GetCountOfTableDescriptors (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","IATSC_STT interface","IATSC_STT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","IATSC_STT.GetCountOfTableDescriptors","IATSC_STT::GetCountOfTableDescriptors","IATSC_STTGetCountOfTableDescriptors","atscpsipparser/IATSC_STT::GetCountOfTableDescriptors","mstv.iatsc_stt_getcountoftabledescriptors"]
old-location: mstv\iatsc_stt_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 527e64b4-c280-46d6-8579-a5755d4b242c
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IATSC_STT.GetCountOfTableDescriptors, IATSC_STT::GetCountOfTableDescriptors, IATSC_STTGetCountOfTableDescriptors, atscpsipparser/IATSC_STT::GetCountOfTableDescriptors, mstv.iatsc_stt_getcountoftabledescriptors
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
 - IATSC_STT::GetCountOfTableDescriptors
 - atscpsipparser/IATSC_STT::GetCountOfTableDescriptors
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
 - IATSC_STT.GetCountOfTableDescriptors
---

# IATSC_STT::GetCountOfTableDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of descriptors in the STT.

## -parameters

### -param pdwVal [out]

Receives the number of descriptors.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_stt">IATSC_STT Interface</a>