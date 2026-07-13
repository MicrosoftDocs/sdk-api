---
UID: NF:mpeg2psiparser.IPMT.QueryServiceGatewayInfo
title: IPMT::QueryServiceGatewayInfo (mpeg2psiparser.h)
description: The QueryServiceGatewayInfo method returns the DSM-CC service gateway information in the PMT, if any.
helpviewer_keywords: ["IPMT interface [Microsoft TV Technologies]","QueryServiceGatewayInfo method","IPMT.QueryServiceGatewayInfo","IPMT::QueryServiceGatewayInfo","IPMTQueryServiceGatewayInfo","QueryServiceGatewayInfo","QueryServiceGatewayInfo method [Microsoft TV Technologies]","QueryServiceGatewayInfo method [Microsoft TV Technologies]","IPMT interface","mpeg2psiparser/IPMT::QueryServiceGatewayInfo","mstv.ipmt_queryservicegatewayinfo"]
old-location: mstv\ipmt_queryservicegatewayinfo.htm
tech.root: mstv
ms.assetid: fead4140-5585-44eb-9d1f-7a686b79ac26
ms.date: 12/05/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],QueryServiceGatewayInfo method, IPMT.QueryServiceGatewayInfo, IPMT::QueryServiceGatewayInfo, IPMTQueryServiceGatewayInfo, QueryServiceGatewayInfo, QueryServiceGatewayInfo method [Microsoft TV Technologies], QueryServiceGatewayInfo method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::QueryServiceGatewayInfo, mstv.ipmt_queryservicegatewayinfo
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
 - IPMT::QueryServiceGatewayInfo
 - mpeg2psiparser/IPMT::QueryServiceGatewayInfo
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
 - IPMT.QueryServiceGatewayInfo
---

# IPMT::QueryServiceGatewayInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>QueryServiceGatewayInfo</b> method returns the DSM-CC service gateway information in the PMT, if any.

## -parameters

### -param ppDSMCCList [out]

Address of a variable that receives a pointer to an array of <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-dsmcc_element">DSMCC_ELEMENT</a> structures. The client must free the array by calling the <b>CoTaskMemFree</b> function.

### -param puiCount [out]

Receives the number of elements returned in <i>ppDSMCCList</i>.

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
<dt><b>MPEG2_S_SG_INFO_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Service gateway information was found in the PMT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_SG_INFO_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Service gateway information was not found in the PMT.

</td>
</tr>
</table>

## -remarks

If the method succeeds, it returns one of the two success codes listed in the previous table. It returns MPEG2_S_SG_INFO_FOUND if the PMT contains service gateway information, or MPEG2_S_SG_INFO_NOT_FOUND if the PMT does not contain any service gateway information.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>