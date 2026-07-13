---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetOrbitalPosition
title: IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetOrbitalPosition","GetOrbitalPosition method [Microsoft TV Technologies]","GetOrbitalPosition method [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetOrbitalPosition method","IDvbSatelliteDeliverySystemDescriptor.GetOrbitalPosition","IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition","IDvbSatelliteDeliverySystemDescriptorGetOrbitalPosition","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition","mstv.idvbsatellitedeliverysystemdescriptor_getorbitalposition"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getorbitalposition.htm
tech.root: mstv
ms.assetid: 1fc3f934-5a9f-4e76-ae1c-e74ea332e8e6
ms.date: 12/05/2018
ms.keywords: GetOrbitalPosition, GetOrbitalPosition method [Microsoft TV Technologies], GetOrbitalPosition method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetOrbitalPosition method, IDvbSatelliteDeliverySystemDescriptor.GetOrbitalPosition, IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition, IDvbSatelliteDeliverySystemDescriptorGetOrbitalPosition, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition, mstv.idvbsatellitedeliverysystemdescriptor_getorbitalposition
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
 - IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition
 - dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition
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
 - IDvbSatelliteDeliverySystemDescriptor.GetOrbitalPosition
---

# IDvbSatelliteDeliverySystemDescriptor::GetOrbitalPosition


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetOrbitalPosition</b> method returns the orbital position.

## -parameters

### -param pwVal [out]

Receives the orbital_position field.

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