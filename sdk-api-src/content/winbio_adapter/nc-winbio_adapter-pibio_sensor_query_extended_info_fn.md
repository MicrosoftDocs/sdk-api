---
UID: NC:winbio_adapter.PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN
title: PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN
author: windows-driver-content
description: Determines the capabilities and limitations of the biometric sensor component.
old-location: secbiomet\sensoradapterqueryextendedinfo.htm
old-project: SecBioMet
ms.assetid: 28CC3757-5A9D-4E29-A26C-6FD90A38B45B
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN, PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN callback, SensorAdapterQueryExtendedInfo, SensorAdapterQueryExtendedInfo callback function [Windows Biometric Framework API], secbiomet.sensoradapterqueryextendedinfo, winbio_adapter/SensorAdapterQueryExtendedInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	SensorAdapterQueryExtendedInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_QUERY_EXTENDED_INFO_FN callback function


## -description


Called by the Windows Biometric Framework to determine the capabilities and limitations of the biometric sensor component.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param SensorInfo [out]

Pointer to the <a href="https://msdn.microsoft.com/37D8BC57-F68D-487A-98B0-94D62CC091C2">WINBIO_EXTENDED_SENSOR_INFO</a> structure that contains the sensor information returned by this function.


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

It will also be called if a client application uses the <a href="https://msdn.microsoft.com/63e38e74-3d46-4474-a31c-eaf724156bc6">WinBioGetProperty</a> function to query the value of the <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property.



