---
UID: NF:mpeg2psiparser.IPMT.QueryMPEInfo
title: IPMT::QueryMPEInfo (mpeg2psiparser.h)
description: The QueryMPEInfo method returns the multi-protocol encapsulation (MPE) information in the PMT, if any.
helpviewer_keywords: ["IPMT interface [Microsoft TV Technologies]","QueryMPEInfo method","IPMT.QueryMPEInfo","IPMT::QueryMPEInfo","IPMTQueryMPEInfo","QueryMPEInfo","QueryMPEInfo method [Microsoft TV Technologies]","QueryMPEInfo method [Microsoft TV Technologies]","IPMT interface","mpeg2psiparser/IPMT::QueryMPEInfo","mstv.ipmt_querympeinfo"]
old-location: mstv\ipmt_querympeinfo.htm
tech.root: mstv
ms.assetid: 14611397-7885-4553-905e-db56404f5e97
ms.date: 12/05/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],QueryMPEInfo method, IPMT.QueryMPEInfo, IPMT::QueryMPEInfo, IPMTQueryMPEInfo, QueryMPEInfo, QueryMPEInfo method [Microsoft TV Technologies], QueryMPEInfo method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::QueryMPEInfo, mstv.ipmt_querympeinfo
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
 - IPMT::QueryMPEInfo
 - mpeg2psiparser/IPMT::QueryMPEInfo
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
 - IPMT.QueryMPEInfo
---

# IPMT::QueryMPEInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>QueryMPEInfo</b> method returns the multi-protocol encapsulation (MPE) information in the PMT, if any.

## -parameters

### -param ppMPEList [out]

Address of a variable that receives a pointer to an array of <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpe_element">MPE_ELEMENT</a> structures. The client must free the array by calling the <b>CoTaskMemFree</b> function.

### -param puiCount [out]

Receives the number of elements returned in <i>ppMPEList</i>.

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
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
Malformed table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MPE_INFO_FOUND</b></dt>
</dl>
</td>
<td width="60%">
MPE information was found in the PMT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MPE_INFO_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
MPE information was not found in the PMT.

</td>
</tr>
</table>

## -remarks

If the method succeeds, it returns one of the two success codes listed in the previous table. It returns MPEG2_S_MPE_INFO_FOUND if the PMT contains MPE information, or MPEG2_S_MPE_INFO_NOT_FOUND if the PMT does not contain any MPE information.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>