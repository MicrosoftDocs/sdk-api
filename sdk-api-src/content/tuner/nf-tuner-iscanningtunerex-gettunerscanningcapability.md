---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IScanningTunerEx::GetTunerScanningCapability


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
 

 

