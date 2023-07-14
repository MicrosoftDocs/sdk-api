---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetTag
title: IDvbSatelliteDeliverySystemDescriptor::GetTag (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbSatelliteDeliverySystemDescriptor.GetTag","IDvbSatelliteDeliverySystemDescriptor::GetTag","IDvbSatelliteDeliverySystemDescriptorGetTag","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetTag","mstv.idvbsatellitedeliverysystemdescriptor_gettag"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 217b49b8-8e98-4784-837d-67471fda2ea5
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbSatelliteDeliverySystemDescriptor.GetTag, IDvbSatelliteDeliverySystemDescriptor::GetTag, IDvbSatelliteDeliverySystemDescriptorGetTag, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetTag, mstv.idvbsatellitedeliverysystemdescriptor_gettag
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
 - IDvbSatelliteDeliverySystemDescriptor::GetTag
 - dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetTag
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
 - IDvbSatelliteDeliverySystemDescriptor.GetTag
---

# IDvbSatelliteDeliverySystemDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTag</b> method returns the descriptor tag.

## -parameters

### -param pbVal [out]

Receives the descriptor tag.

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