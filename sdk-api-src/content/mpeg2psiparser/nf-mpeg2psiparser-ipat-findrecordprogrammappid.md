---
UID: NF:mpeg2psiparser.IPAT.FindRecordProgramMapPid
title: IPAT::FindRecordProgramMapPid (mpeg2psiparser.h)
description: The FindRecordProgramMapPid method returns the packet identifier (PID) for the program map table (PMT) associated with a given program number.
helpviewer_keywords: ["FindRecordProgramMapPid","FindRecordProgramMapPid method [Microsoft TV Technologies]","FindRecordProgramMapPid method [Microsoft TV Technologies]","IPAT interface","IPAT interface [Microsoft TV Technologies]","FindRecordProgramMapPid method","IPAT.FindRecordProgramMapPid","IPAT::FindRecordProgramMapPid","IPATFindRecordProgramMapPid","mpeg2psiparser/IPAT::FindRecordProgramMapPid","mstv.ipat_findrecordprogrammappid"]
old-location: mstv\ipat_findrecordprogrammappid.htm
tech.root: mstv
ms.assetid: 148cb123-7cac-46a8-8d60-ce2a28e89230
ms.date: 12/05/2018
ms.keywords: FindRecordProgramMapPid, FindRecordProgramMapPid method [Microsoft TV Technologies], FindRecordProgramMapPid method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],FindRecordProgramMapPid method, IPAT.FindRecordProgramMapPid, IPAT::FindRecordProgramMapPid, IPATFindRecordProgramMapPid, mpeg2psiparser/IPAT::FindRecordProgramMapPid, mstv.ipat_findrecordprogrammappid
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
 - IPAT::FindRecordProgramMapPid
 - mpeg2psiparser/IPAT::FindRecordProgramMapPid
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
 - IPAT.FindRecordProgramMapPid
---

# IPAT::FindRecordProgramMapPid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>FindRecordProgramMapPid</b> method returns the packet identifier (PID) for the program map table (PMT) associated with a given program number.

## -parameters

### -param wProgramNumber [in]

Specifies the program number.

### -param pwVal [out]

Receives the PID.

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
<dt><b>MPEG2_E_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The table does not contain the specified program number.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipat">IPAT Interface</a>