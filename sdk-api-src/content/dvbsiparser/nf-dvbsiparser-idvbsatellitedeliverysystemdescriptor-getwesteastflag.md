---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag
title: IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetWestEastFlag","GetWestEastFlag method [Microsoft TV Technologies]","GetWestEastFlag method [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetWestEastFlag method","IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag","IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag","IDvbSatelliteDeliverySystemDescriptorGetWestEastFlag","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag","mstv.idvbsatellitedeliverysystemdescriptor_getwesteastflag"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getwesteastflag.htm
tech.root: mstv
ms.assetid: 533a2ed4-f5ac-4f41-a03b-0b274f327436
ms.date: 12/05/2018
ms.keywords: GetWestEastFlag, GetWestEastFlag method [Microsoft TV Technologies], GetWestEastFlag method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetWestEastFlag method, IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag, IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag, IDvbSatelliteDeliverySystemDescriptorGetWestEastFlag, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag, mstv.idvbsatellitedeliverysystemdescriptor_getwesteastflag
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
 - IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag
 - dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag
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
 - IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag
---

# IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetWestEastFlag</b> method returns a flag that specifies whether the satellite is in the western or eastern part of the orbit.

## -parameters

### -param pbVal [out]

Receives the west_east_flag field.

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