---
UID: NF:atscpsipparser.IATSC_ETT.GetVersionNumber
title: IATSC_ETT::GetVersionNumber (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IATSC_ETT interface","IATSC_ETT interface [Microsoft TV Technologies]","GetVersionNumber method","IATSC_ETT.GetVersionNumber","IATSC_ETT::GetVersionNumber","IATSC_ETTGetVersionNumber","atscpsipparser/IATSC_ETT::GetVersionNumber","mstv.iatsc_ett_getversionnumber"]
old-location: mstv\iatsc_ett_getversionnumber.htm
tech.root: mstv
ms.assetid: bd9eefda-51ff-472c-b363-2f3c21ae2fec
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IATSC_ETT interface, IATSC_ETT interface [Microsoft TV Technologies],GetVersionNumber method, IATSC_ETT.GetVersionNumber, IATSC_ETT::GetVersionNumber, IATSC_ETTGetVersionNumber, atscpsipparser/IATSC_ETT::GetVersionNumber, mstv.iatsc_ett_getversionnumber
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
 - IATSC_ETT::GetVersionNumber
 - atscpsipparser/IATSC_ETT::GetVersionNumber
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
 - IATSC_ETT.GetVersionNumber
---

# IATSC_ETT::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVersionNumber</b> method returns the version number for the ETT.

## -parameters

### -param pbVal [out]

Receives the version_number field.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_ett">IATSC_ETT Interface</a>