---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetGuardInterval
title: IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval (dvbsiparser.h)
description: Gets the guard interval from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
helpviewer_keywords: ["GetGuardInterval","GetGuardInterval method [Microsoft TV Technologies]","GetGuardInterval method [Microsoft TV Technologies]","IIsdbTerrestrialDeliverySystemDescriptor interface","IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetGuardInterval method","IIsdbTerrestrialDeliverySystemDescriptor.GetGuardInterval","IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval","dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval","mstv.iisdbterrestrialdeliverysystemdescriptor_getguardinterval"]
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_getguardinterval.htm
tech.root: mstv
ms.assetid: f1016fd4-bcd9-4678-b59c-c6c8207f242d
ms.date: 12/05/2018
ms.keywords: GetGuardInterval, GetGuardInterval method [Microsoft TV Technologies], GetGuardInterval method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetGuardInterval method, IIsdbTerrestrialDeliverySystemDescriptor.GetGuardInterval, IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval, mstv.iisdbterrestrialdeliverysystemdescriptor_getguardinterval
req.header: dvbsiparser.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval
 - dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval
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
 - IIsdbTerrestrialDeliverySystemDescriptor.GetGuardInterval
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetGuardInterval


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the guard interval from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor. The guard interval specifies the fraction of an orthogonal frequency division multiplexing (OFDM) symbol period that separates each pair of OFDM symbols.

## -parameters

### -param pbVal [out]

Receives the code indicating the guard value. This code can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
1/32

</td>
</tr>
</table>
 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
1/16

</td>
</tr>
</table>
 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
1/8

</td>
</tr>
</table>
 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
1/4

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor">IIsdbTerrestrialDeliverySystemDescriptor</a>