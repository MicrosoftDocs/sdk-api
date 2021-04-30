---
UID: NF:atscpsipparser.IATSC_VCT.GetVersionNumber
title: IATSC_VCT::GetVersionNumber (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetVersionNumber method","IATSC_VCT.GetVersionNumber","IATSC_VCT::GetVersionNumber","IATSC_VCTGetVersionNumber","atscpsipparser/IATSC_VCT::GetVersionNumber","mstv.iatsc_vct_getversionnumber"]
old-location: mstv\iatsc_vct_getversionnumber.htm
tech.root: mstv
ms.assetid: c89e2fde-958f-4193-84d9-2d98e7560c6a
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetVersionNumber method, IATSC_VCT.GetVersionNumber, IATSC_VCT::GetVersionNumber, IATSC_VCTGetVersionNumber, atscpsipparser/IATSC_VCT::GetVersionNumber, mstv.iatsc_vct_getversionnumber
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
 - IATSC_VCT::GetVersionNumber
 - atscpsipparser/IATSC_VCT::GetVersionNumber
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
 - IATSC_VCT.GetVersionNumber
---

# IATSC_VCT::GetVersionNumber


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVersionNumber</b> method returns the version number for the VCT.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>