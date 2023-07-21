---
UID: NF:dvbsiparser.IDVB_NIT.GetNetworkId
title: IDVB_NIT::GetNetworkId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetNetworkId","GetNetworkId method [Microsoft TV Technologies]","GetNetworkId method [Microsoft TV Technologies]","IDVB_NIT interface","IDVB_NIT interface [Microsoft TV Technologies]","GetNetworkId method","IDVB_NIT.GetNetworkId","IDVB_NIT::GetNetworkId","IDVB_NITGetNetworkId","dvbsiparser/IDVB_NIT::GetNetworkId","mstv.idvb_nit_getnetworkid"]
old-location: mstv\idvb_nit_getnetworkid.htm
tech.root: mstv
ms.assetid: 86841b62-d6c0-4911-baf7-dd6d1a08a770
ms.date: 12/05/2018
ms.keywords: GetNetworkId, GetNetworkId method [Microsoft TV Technologies], GetNetworkId method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetNetworkId method, IDVB_NIT.GetNetworkId, IDVB_NIT::GetNetworkId, IDVB_NITGetNetworkId, dvbsiparser/IDVB_NIT::GetNetworkId, mstv.idvb_nit_getnetworkid
req.header: dvbsiparser.h
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
 - IDVB_NIT::GetNetworkId
 - dvbsiparser/IDVB_NIT::GetNetworkId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_NIT.GetNetworkId
---

# IDVB_NIT::GetNetworkId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNetworkId</b> method returns the network identifier for the NIT.

## -parameters

### -param pwVal [out]

Pointer to a variable that receives the network_id field.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT Interface</a>