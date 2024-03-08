---
UID: NF:dvbsiparser.IDvbCableDeliverySystemDescriptor.GetFECOuter
title: IDvbCableDeliverySystemDescriptor::GetFECOuter (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetFECOuter","GetFECOuter method [Microsoft TV Technologies]","GetFECOuter method [Microsoft TV Technologies]","IDvbCableDeliverySystemDescriptor interface","IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetFECOuter method","IDvbCableDeliverySystemDescriptor.GetFECOuter","IDvbCableDeliverySystemDescriptor::GetFECOuter","IDvbCableDeliverySystemDescriptorGetFECOuter","dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECOuter","mstv.idvbcabledeliverysystemdescriptor_getfecouter"]
old-location: mstv\idvbcabledeliverysystemdescriptor_getfecouter.htm
tech.root: mstv
ms.assetid: cf6d094f-d394-43a3-b74e-a167759d5a10
ms.date: 12/05/2018
ms.keywords: GetFECOuter, GetFECOuter method [Microsoft TV Technologies], GetFECOuter method [Microsoft TV Technologies],IDvbCableDeliverySystemDescriptor interface, IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies],GetFECOuter method, IDvbCableDeliverySystemDescriptor.GetFECOuter, IDvbCableDeliverySystemDescriptor::GetFECOuter, IDvbCableDeliverySystemDescriptorGetFECOuter, dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECOuter, mstv.idvbcabledeliverysystemdescriptor_getfecouter
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
 - IDvbCableDeliverySystemDescriptor::GetFECOuter
 - dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECOuter
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
 - IDvbCableDeliverySystemDescriptor.GetFECOuter
---

# IDvbCableDeliverySystemDescriptor::GetFECOuter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetFECOuter</b> method returns the output forward error correction (FEC) scheme.

## -parameters

### -param pbVal [out]

Receives the FEC_outer field.

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