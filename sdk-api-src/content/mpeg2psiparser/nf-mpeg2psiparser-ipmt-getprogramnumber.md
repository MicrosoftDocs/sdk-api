---
UID: NF:mpeg2psiparser.IPMT.GetProgramNumber
title: IPMT::GetProgramNumber (mpeg2psiparser.h)
description: The GetProgramNumber method returns the program number for the PMT.
helpviewer_keywords: ["GetProgramNumber","GetProgramNumber method [Microsoft TV Technologies]","GetProgramNumber method [Microsoft TV Technologies]","IPMT interface","IPMT interface [Microsoft TV Technologies]","GetProgramNumber method","IPMT.GetProgramNumber","IPMT::GetProgramNumber","IPMTGetProgramNumber","mpeg2psiparser/IPMT::GetProgramNumber","mstv.ipmt_getprogramnumber"]
old-location: mstv\ipmt_getprogramnumber.htm
tech.root: mstv
ms.assetid: 39006f8b-7dd4-4f19-badc-3a288a7b6520
ms.date: 12/05/2018
ms.keywords: GetProgramNumber, GetProgramNumber method [Microsoft TV Technologies], GetProgramNumber method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetProgramNumber method, IPMT.GetProgramNumber, IPMT::GetProgramNumber, IPMTGetProgramNumber, mpeg2psiparser/IPMT::GetProgramNumber, mstv.ipmt_getprogramnumber
req.header: mpeg2psiparser.h
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
 - IPMT::GetProgramNumber
 - mpeg2psiparser/IPMT::GetProgramNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetProgramNumber
---

# IPMT::GetProgramNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetProgramNumber</b> method returns the program number for the PMT.

## -parameters

### -param pwVal [out]

Receives the program_number field.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>