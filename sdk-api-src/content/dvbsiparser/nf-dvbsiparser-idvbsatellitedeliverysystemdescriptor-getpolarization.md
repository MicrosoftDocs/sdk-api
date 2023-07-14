---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetPolarization
title: IDvbSatelliteDeliverySystemDescriptor::GetPolarization (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetPolarization","GetPolarization method [Microsoft TV Technologies]","GetPolarization method [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetPolarization method","IDvbSatelliteDeliverySystemDescriptor.GetPolarization","IDvbSatelliteDeliverySystemDescriptor::GetPolarization","IDvbSatelliteDeliverySystemDescriptorGetPolarization","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetPolarization","mstv.idvbsatellitedeliverysystemdescriptor_getpolarization"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getpolarization.htm
tech.root: mstv
ms.assetid: fe063a08-74bd-40c4-a185-3cc932a0a06d
ms.date: 12/05/2018
ms.keywords: GetPolarization, GetPolarization method [Microsoft TV Technologies], GetPolarization method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetPolarization method, IDvbSatelliteDeliverySystemDescriptor.GetPolarization, IDvbSatelliteDeliverySystemDescriptor::GetPolarization, IDvbSatelliteDeliverySystemDescriptorGetPolarization, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetPolarization, mstv.idvbsatellitedeliverysystemdescriptor_getpolarization
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
 - IDvbSatelliteDeliverySystemDescriptor::GetPolarization
 - dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetPolarization
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
 - IDvbSatelliteDeliverySystemDescriptor.GetPolarization
---

# IDvbSatelliteDeliverySystemDescriptor::GetPolarization


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetPolarization</b> method returns the polarization of the transmitted signal.

## -parameters

### -param pbVal [out]

Receives the polarization field.

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