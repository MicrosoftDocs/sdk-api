---
UID: NF:mpeg2psiparser.IPAT.GetCountOfRecords
title: IPAT::GetCountOfRecords (mpeg2psiparser.h)
description: The GetCountOfRecords method returns the number of records in the PAT. Each record corresponds to one program.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IPAT interface","IPAT interface [Microsoft TV Technologies]","GetCountOfRecords method","IPAT.GetCountOfRecords","IPAT::GetCountOfRecords","IPATGetCountOfRecords","mpeg2psiparser/IPAT::GetCountOfRecords","mstv.ipat_getcountofrecords"]
old-location: mstv\ipat_getcountofrecords.htm
tech.root: mstv
ms.assetid: 6b73a02e-d6dd-402b-baca-8728cd0fa900
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetCountOfRecords method, IPAT.GetCountOfRecords, IPAT::GetCountOfRecords, IPATGetCountOfRecords, mpeg2psiparser/IPAT::GetCountOfRecords, mstv.ipat_getcountofrecords
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
 - IPAT::GetCountOfRecords
 - mpeg2psiparser/IPAT::GetCountOfRecords
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
 - IPAT.GetCountOfRecords
---

# IPAT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetCountOfRecords</b> method returns the number of records in the PAT. Each record corresponds to one program.

## -parameters

### -param pdwVal [out]

Receives the number of records.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipat">IPAT Interface</a>