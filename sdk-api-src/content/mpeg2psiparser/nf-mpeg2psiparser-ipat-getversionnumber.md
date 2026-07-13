---
UID: NF:mpeg2psiparser.IPAT.GetVersionNumber
title: IPAT::GetVersionNumber (mpeg2psiparser.h)
description: The GetVersionNumber method returns the version number for the PAT.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IPAT interface","IPAT interface [Microsoft TV Technologies]","GetVersionNumber method","IPAT.GetVersionNumber","IPAT::GetVersionNumber","IPATGetVersionNumber","mpeg2psiparser/IPAT::GetVersionNumber","mstv.ipat_getversionnumber"]
old-location: mstv\ipat_getversionnumber.htm
tech.root: mstv
ms.assetid: 1398a1b9-e9b9-4f30-ba93-0a08a0994cf9
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetVersionNumber method, IPAT.GetVersionNumber, IPAT::GetVersionNumber, IPATGetVersionNumber, mpeg2psiparser/IPAT::GetVersionNumber, mstv.ipat_getversionnumber
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
 - IPAT::GetVersionNumber
 - mpeg2psiparser/IPAT::GetVersionNumber
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
 - IPAT.GetVersionNumber
---

# IPAT::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetVersionNumber</b> method returns the version number for the PAT.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipat">IPAT Interface</a>