---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetSymbolRate
title: IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetSymbolRate","GetSymbolRate method [Microsoft TV Technologies]","GetSymbolRate method [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetSymbolRate method","IDvbSatelliteDeliverySystemDescriptor.GetSymbolRate","IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate","IDvbSatelliteDeliverySystemDescriptorGetSymbolRate","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate","mstv.idvbsatellitedeliverysystemdescriptor_getsymbolrate"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getsymbolrate.htm
tech.root: mstv
ms.assetid: 184b1cb6-432a-4227-b711-e05201f80bf1
ms.date: 12/05/2018
ms.keywords: GetSymbolRate, GetSymbolRate method [Microsoft TV Technologies], GetSymbolRate method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetSymbolRate method, IDvbSatelliteDeliverySystemDescriptor.GetSymbolRate, IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate, IDvbSatelliteDeliverySystemDescriptorGetSymbolRate, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate, mstv.idvbsatellitedeliverysystemdescriptor_getsymbolrate
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
 - IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate
 - dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate
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
 - IDvbSatelliteDeliverySystemDescriptor.GetSymbolRate
---

# IDvbSatelliteDeliverySystemDescriptor::GetSymbolRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsatellitedeliverysystemdescriptor">IDvbSatelliteDeliverySystemDescriptor Interface</a>