---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetCAUnitId
title: IIsdbCAContractInformationDescriptor::GetCAUnitId (dvbsiparser.h)
description: Gets the value of the CA_unit_id field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field identifies the billing or nonbilling unit to which the component belongs.
helpviewer_keywords: ["GetCAUnitId","GetCAUnitId method [Microsoft TV Technologies]","GetCAUnitId method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetCAUnitId method","IIsdbCAContractInformationDescriptor.GetCAUnitId","IIsdbCAContractInformationDescriptor::GetCAUnitId","dvbsiparser/IIsdbCAContractInformationDescriptor::GetCAUnitId","mstv.iisdbcacontractinformationdescriptor_getcaunitid"]
old-location: mstv\iisdbcacontractinformationdescriptor_getcaunitid.htm
tech.root: mstv
ms.assetid: 1e50f417-6403-499a-944c-2926a18dada1
ms.date: 12/05/2018
ms.keywords: GetCAUnitId, GetCAUnitId method [Microsoft TV Technologies], GetCAUnitId method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetCAUnitId method, IIsdbCAContractInformationDescriptor.GetCAUnitId, IIsdbCAContractInformationDescriptor::GetCAUnitId, dvbsiparser/IIsdbCAContractInformationDescriptor::GetCAUnitId, mstv.iisdbcacontractinformationdescriptor_getcaunitid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbCAContractInformationDescriptor::GetCAUnitId
 - dvbsiparser/IIsdbCAContractInformationDescriptor::GetCAUnitId
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
 - IIsdbCAContractInformationDescriptor.GetCAUnitId
---

# IIsdbCAContractInformationDescriptor::GetCAUnitId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the value of the CA_unit_id field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field identifies the billing or nonbilling unit to which the component belongs.

## -parameters

### -param pbVal [out]

Receives the conditional access unit identifier. This can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Nonbilling unit group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Billing unit group including default event ES group. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x2 - 0xF</dt>
</dl>
</td>
<td width="60%">
Billing unit group other than the default event ES group.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>