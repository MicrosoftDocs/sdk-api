---
UID: NF:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor.GetOtherFrequencyFlag
title: IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetOtherFrequencyFlag","GetOtherFrequencyFlag method [Microsoft TV Technologies]","GetOtherFrequencyFlag method [Microsoft TV Technologies]","IDvbTerrestrialDeliverySystemDescriptor interface","IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetOtherFrequencyFlag method","IDvbTerrestrialDeliverySystemDescriptor.GetOtherFrequencyFlag","IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag","IDvbTerrestrialDeliverySystemDescriptorGetOtherFrequencyFlag","dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag","mstv.idvbterrestrialdeliverysystemdescriptor_getotherfrequencyflag"]
old-location: mstv\idvbterrestrialdeliverysystemdescriptor_getotherfrequencyflag.htm
tech.root: mstv
ms.assetid: 1462004c-7605-430e-bf9a-beb1776adb6c
ms.date: 12/05/2018
ms.keywords: GetOtherFrequencyFlag, GetOtherFrequencyFlag method [Microsoft TV Technologies], GetOtherFrequencyFlag method [Microsoft TV Technologies],IDvbTerrestrialDeliverySystemDescriptor interface, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetOtherFrequencyFlag method, IDvbTerrestrialDeliverySystemDescriptor.GetOtherFrequencyFlag, IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag, IDvbTerrestrialDeliverySystemDescriptorGetOtherFrequencyFlag, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag, mstv.idvbterrestrialdeliverysystemdescriptor_getotherfrequencyflag
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
 - IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag
 - dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag
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
 - IDvbTerrestrialDeliverySystemDescriptor.GetOtherFrequencyFlag
---

# IDvbTerrestrialDeliverySystemDescriptor::GetOtherFrequencyFlag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetOtherFrequencyFlag</b> method returns a flag that specifies whether other frequencies are in use.

## -parameters

### -param pbVal [out]

Receives the other_frequency_flag field.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbterrestrialdeliverysystemdescriptor">IDvbTerrestrialDeliverySystemDescriptor Interface</a>