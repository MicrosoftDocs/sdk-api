---
UID: NF:atscpsipparser.IATSC_EIT.GetSourceId
title: IATSC_EIT::GetSourceId (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetSourceId","GetSourceId method [Microsoft TV Technologies]","GetSourceId method [Microsoft TV Technologies]","IATSC_EIT interface","IATSC_EIT interface [Microsoft TV Technologies]","GetSourceId method","IATSC_EIT.GetSourceId","IATSC_EIT::GetSourceId","IATSC_EITGetSourceId","atscpsipparser/IATSC_EIT::GetSourceId","mstv.iatsc_eit_getsourceid"]
old-location: mstv\iatsc_eit_getsourceid.htm
tech.root: mstv
ms.assetid: 2ab6709e-3d96-4388-a9b2-97a2f04a4eae
ms.date: 12/05/2018
ms.keywords: GetSourceId, GetSourceId method [Microsoft TV Technologies], GetSourceId method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetSourceId method, IATSC_EIT.GetSourceId, IATSC_EIT::GetSourceId, IATSC_EITGetSourceId, atscpsipparser/IATSC_EIT::GetSourceId, mstv.iatsc_eit_getsourceid
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
 - IATSC_EIT::GetSourceId
 - atscpsipparser/IATSC_EIT::GetSourceId
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
 - IATSC_EIT.GetSourceId
---

# IATSC_EIT::GetSourceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSourceId</b> method returns the source identifier for the EIT.

## -parameters

### -param pwVal [out]

Receives the source_id field.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_eit">IATSC_EIT Interface</a>