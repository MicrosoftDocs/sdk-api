---
UID: NF:dvbsiparser.IDVB_EIT.GetServiceId
title: IDVB_EIT::GetServiceId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetServiceId","GetServiceId method [Microsoft TV Technologies]","GetServiceId method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","GetServiceId method","IDVB_EIT.GetServiceId","IDVB_EIT::GetServiceId","IDVB_EITGetServiceId","dvbsiparser/IDVB_EIT::GetServiceId","mstv.idvb_eit_getserviceid"]
old-location: mstv\idvb_eit_getserviceid.htm
tech.root: mstv
ms.assetid: 6ff89d80-9c68-4c2a-b0b5-14603b55d7b7
ms.date: 12/05/2018
ms.keywords: GetServiceId, GetServiceId method [Microsoft TV Technologies], GetServiceId method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetServiceId method, IDVB_EIT.GetServiceId, IDVB_EIT::GetServiceId, IDVB_EITGetServiceId, dvbsiparser/IDVB_EIT::GetServiceId, mstv.idvb_eit_getserviceid
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
 - IDVB_EIT::GetServiceId
 - dvbsiparser/IDVB_EIT::GetServiceId
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
 - IDVB_EIT.GetServiceId
---

# IDVB_EIT::GetServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetServiceId</b> method returns the service identifier, which distinguishes the service from other services carried in the transport stream.

## -parameters

### -param pwVal [out]

Pointer to a variable that receives the service_id field.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>