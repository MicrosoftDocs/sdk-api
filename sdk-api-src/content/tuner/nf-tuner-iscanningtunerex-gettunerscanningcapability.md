---
UID: NF:tuner.IScanningTunerEx.GetTunerScanningCapability
title: IScanningTunerEx::GetTunerScanningCapability method
author: windows-driver-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_gettunerscanningcapability.htm
old-project: mstv
ms.assetid: 7dc7aeec-2a9d-4dfb-9f67-36d8131cc130
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTunerScanningCapability method [Microsoft TV Technologies], GetTunerScanningCapability method [Microsoft TV Technologies], IScanningTunerEx interface, GetTunerScanningCapability,IScanningTunerEx.GetTunerScanningCapability, IScanningTunerEx, IScanningTunerEx interface [Microsoft TV Technologies], GetTunerScanningCapability method, IScanningTunerEx::GetTunerScanningCapability, IScanningTunerExGetTunerScanningCapability, mstv.iscanningtunerex_gettunerscanningcapability, tuner/IScanningTunerEx::GetTunerScanningCapability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tuner.h
api_name:
-	IScanningTunerEx.GetTunerScanningCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTunerEx::GetTunerScanningCapability method


## -description



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
<th>
              Description
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




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

