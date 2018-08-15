---
UID: NF:dvbsiparser.IDvbCableDeliverySystemDescriptor.GetSymbolRate
title: IDvbCableDeliverySystemDescriptor::GetSymbolRate
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbcabledeliverysystemdescriptor_getsymbolrate.htm
old-project: mstv
ms.assetid: 0484e12d-6b93-4ed6-865a-d4992ad1de75
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSymbolRate, GetSymbolRate method [Microsoft TV Technologies], GetSymbolRate method [Microsoft TV Technologies],IDvbCableDeliverySystemDescriptor interface, IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies],GetSymbolRate method, IDvbCableDeliverySystemDescriptor.GetSymbolRate, IDvbCableDeliverySystemDescriptor::GetSymbolRate, IDvbCableDeliverySystemDescriptorGetSymbolRate, dvbsiparser/IDvbCableDeliverySystemDescriptor::GetSymbolRate, mstv.idvbcabledeliverysystemdescriptor_getsymbolrate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.redist: 
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
 - IDvbCableDeliverySystemDescriptor.GetSymbolRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbCableDeliverySystemDescriptor::GetSymbolRate


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSymbolRate</b> method returns the symbol rate.


## -parameters




### -param pdwVal [out]

Receives the symbol_rate field.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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




<a href="https://msdn.microsoft.com/b4fb2fd0-e32a-4737-8095-7d4df40a26a0">IDvbCableDeliverySystemDescriptor Interface</a>
 

 

