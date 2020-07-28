---
UID: NC:winbio_adapter.PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN
title: PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN (winbio_adapter.h)
description: Determines the capabilities and limitations of the biometric sensor component.
helpviewer_keywords: ["PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN","PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN callback","SensorAdapterQueryExtendedInfo","SensorAdapterQueryExtendedInfo callback function [Windows Biometric Framework API]","secbiomet.sensoradapterqueryextendedinfo","winbio_adapter/SensorAdapterQueryExtendedInfo"]
old-location: secbiomet\sensoradapterqueryextendedinfo.htm
tech.root: SecBioMet
ms.assetid: 28CC3757-5A9D-4E29-A26C-6FD90A38B45B
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN, PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN callback, SensorAdapterQueryExtendedInfo, SensorAdapterQueryExtendedInfo callback function [Windows Biometric Framework API], secbiomet.sensoradapterqueryextendedinfo, winbio_adapter/SensorAdapterQueryExtendedInfo
f1_keywords:
- winbio_adapter/SensorAdapterQueryExtendedInfo
dev_langs:
- c++
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- SensorAdapterQueryExtendedInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN callback function


## -description


Called by the Windows Biometric Framework to determine the capabilities and limitations of the biometric sensor component.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param SensorInfo [out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/SecBioMet/winbio-extended-sensor-info">WINBIO_EXTENDED_SENSOR_INFO</a> structure that contains the sensor information returned by this function.


### -param SensorInfoSize [in]

The specified size of the sensor information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> and <i>SensorInfo</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>SensorInfoSize</i> value is less than the size needed to return the sensor information.

</td>
</tr>
</table>
 




## -remarks



This method is called once during configuration of the biometric unit. 

It will also be called if a client application uses the <a href="https://docs.microsoft.com/windows/desktop/api/winbio/nf-winbio-winbiogetproperty">WinBioGetProperty</a> function to query the value of the <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property.



