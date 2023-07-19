---
UID: NF:tuner.IScanningTunerEx.GetTunerScanningCapability
title: IScanningTunerEx::GetTunerScanningCapability (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["GetTunerScanningCapability","GetTunerScanningCapability method [Microsoft TV Technologies]","GetTunerScanningCapability method [Microsoft TV Technologies]","IScanningTunerEx interface","IScanningTunerEx interface [Microsoft TV Technologies]","GetTunerScanningCapability method","IScanningTunerEx.GetTunerScanningCapability","IScanningTunerEx::GetTunerScanningCapability","IScanningTunerExGetTunerScanningCapability","mstv.iscanningtunerex_gettunerscanningcapability","tuner/IScanningTunerEx::GetTunerScanningCapability"]
old-location: mstv\iscanningtunerex_gettunerscanningcapability.htm
tech.root: mstv
ms.assetid: 7dc7aeec-2a9d-4dfb-9f67-36d8131cc130
ms.date: 12/05/2018
ms.keywords: GetTunerScanningCapability, GetTunerScanningCapability method [Microsoft TV Technologies], GetTunerScanningCapability method [Microsoft TV Technologies],IScanningTunerEx interface, IScanningTunerEx interface [Microsoft TV Technologies],GetTunerScanningCapability method, IScanningTunerEx.GetTunerScanningCapability, IScanningTunerEx::GetTunerScanningCapability, IScanningTunerExGetTunerScanningCapability, mstv.iscanningtunerex_gettunerscanningcapability, tuner/IScanningTunerEx::GetTunerScanningCapability
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IScanningTunerEx::GetTunerScanningCapability
 - tuner/IScanningTunerEx::GetTunerScanningCapability
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tuner.h
api_name:
 - IScanningTunerEx.GetTunerScanningCapability
---

# IScanningTunerEx::GetTunerScanningCapability


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista and later.
        



The <b>GetTunerScanningCapability</b> method retrieves the set of broadcast standards supported by the tuner and the tuner's scanning capability.

## -parameters

### -param HardwareAssistedScanning [out]

Receives a Boolean value. If the value is <b>TRUE</b>, the scanning algorithm is implemented entirely by the tuner hardware. Otherwise, the tuner filter implements part of the scanning algorithm in software.

### -param NumStandardsSupported [out]

Receives the number of broadcast standards supported by the tuner.

### -param BroadcastStandards [out]

Pointer to an array of GUIDs. The array must be large enough to hold a number of elements equal to the value returned in the <i>NumStandardsSupported</i> parameter. To find the required array size, call the method once and set this parameter to <b>NULL</b>. Then allocate the array and call the method again, setting this parameter to the address of the array.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

The following broadcast standard GUIDs are defined in Bdamedia.h.

<table>
<tr>
<th><b>GUID</b></th>
<th>Description
            </th>
</tr>
<tr>
<td>ANALOG_AUXIN_NETWORK_TYPE</td>
<td>Auxiliary video input</td>
</tr>
<tr>
<td>ANALOG_FM_NETWORK_TYPE</td>
<td>FM radio tuner</td>
</tr>
<tr>
<td>ANALOG_TV_NETWORK_TYPE</td>
<td>Analog television</td>
</tr>
<tr>
<td>DIGITAL_CABLE_NETWORK_TYPE</td>
<td>Digital cable</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>