---
UID: NF:dvbsiparser.IDvbCableDeliverySystemDescriptor.GetFECInner
title: IDvbCableDeliverySystemDescriptor::GetFECInner (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetFECInner","GetFECInner method [Microsoft TV Technologies]","GetFECInner method [Microsoft TV Technologies]","IDvbCableDeliverySystemDescriptor interface","IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetFECInner method","IDvbCableDeliverySystemDescriptor.GetFECInner","IDvbCableDeliverySystemDescriptor::GetFECInner","IDvbCableDeliverySystemDescriptorGetFECInner","dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECInner","mstv.idvbcabledeliverysystemdescriptor_getfecinner"]
old-location: mstv\idvbcabledeliverysystemdescriptor_getfecinner.htm
tech.root: mstv
ms.assetid: 6b16b904-58aa-4f28-83aa-80dd625d387a
ms.date: 12/05/2018
ms.keywords: GetFECInner, GetFECInner method [Microsoft TV Technologies], GetFECInner method [Microsoft TV Technologies],IDvbCableDeliverySystemDescriptor interface, IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies],GetFECInner method, IDvbCableDeliverySystemDescriptor.GetFECInner, IDvbCableDeliverySystemDescriptor::GetFECInner, IDvbCableDeliverySystemDescriptorGetFECInner, dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECInner, mstv.idvbcabledeliverysystemdescriptor_getfecinner
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
 - IDvbCableDeliverySystemDescriptor::GetFECInner
 - dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECInner
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
 - IDvbCableDeliverySystemDescriptor.GetFECInner
---

# IDvbCableDeliverySystemDescriptor::GetFECInner


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetFECInner</b> method returns the inner forward error correction (FEC) scheme.

## -parameters

### -param pbVal [out]

Receives the FEC_inner field.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcabledeliverysystemdescriptor">IDvbCableDeliverySystemDescriptor Interface</a>