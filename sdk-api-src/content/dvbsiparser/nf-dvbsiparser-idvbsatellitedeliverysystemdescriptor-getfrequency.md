---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetFrequency
title: IDvbSatelliteDeliverySystemDescriptor::GetFrequency (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetFrequency","GetFrequency method [Microsoft TV Technologies]","GetFrequency method [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetFrequency method","IDvbSatelliteDeliverySystemDescriptor.GetFrequency","IDvbSatelliteDeliverySystemDescriptor::GetFrequency","IDvbSatelliteDeliverySystemDescriptorGetFrequency","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetFrequency","mstv.idvbsatellitedeliverysystemdescriptor_getfrequency"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getfrequency.htm
tech.root: mstv
ms.assetid: dc298f61-f7f1-42dc-a585-bfe9f58b1629
ms.date: 12/05/2018
ms.keywords: GetFrequency, GetFrequency method [Microsoft TV Technologies], GetFrequency method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetFrequency method, IDvbSatelliteDeliverySystemDescriptor.GetFrequency, IDvbSatelliteDeliverySystemDescriptor::GetFrequency, IDvbSatelliteDeliverySystemDescriptorGetFrequency, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetFrequency, mstv.idvbsatellitedeliverysystemdescriptor_getfrequency
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbSatelliteDeliverySystemDescriptor::GetFrequency
 - dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetFrequency
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
 - IDvbSatelliteDeliverySystemDescriptor.GetFrequency
---

# IDvbSatelliteDeliverySystemDescriptor::GetFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetFrequency</b> method returns the frequency.

## -parameters

### -param pdwVal [out]

Receives the frequency field.

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