---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetCAUnitId
title: IIsdbCAContractInformationDescriptor::GetCAUnitId
author: windows-sdk-content
description: Gets the value of the CA_unit_id field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field identifies the billing or nonbilling unit to which the component belongs.
old-location: mstv\iisdbcacontractinformationdescriptor_getcaunitid.htm
old-project: mstv
ms.assetid: 1e50f417-6403-499a-944c-2926a18dada1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCAUnitId, GetCAUnitId method [Microsoft TV Technologies], GetCAUnitId method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetCAUnitId method, IIsdbCAContractInformationDescriptor.GetCAUnitId, IIsdbCAContractInformationDescriptor::GetCAUnitId, dvbsiparser/IIsdbCAContractInformationDescriptor::GetCAUnitId, mstv.iisdbcacontractinformationdescriptor_getcaunitid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbCAContractInformationDescriptor.GetCAUnitId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbCAContractInformationDescriptor::GetCAUnitId


## -description


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d877a625-d683-4472-98de-f24c165c753a">IIsdbCAContractInformationDescriptor</a>
 

 

