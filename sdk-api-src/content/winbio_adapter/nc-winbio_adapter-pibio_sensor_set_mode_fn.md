---
UID: NC:winbio_adapter.PIBIO_SENSOR_SET_MODE_FN
title: PIBIO_SENSOR_SET_MODE_FN
author: windows-sdk-content
description: Sets the sensor adapter mode.
old-location: secbiomet\sensoradaptersetmode.htm
tech.root: SecBioMet
ms.assetid: 83c4ecfa-da4f-41d3-b0ca-d654735743cd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PIBIO_SENSOR_SET_MODE_FN, PIBIO_SENSOR_SET_MODE_FN callback, SensorAdapterSetMode, SensorAdapterSetMode callback function [Windows Biometric Framework API], secbiomet.sensoradaptersetmode, winbio_adapter/SensorAdapterSetMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - SensorAdapterSetMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_SENSOR_SET_MODE_FN callback function


## -description


Called by the Windows Biometric Framework to set the sensor adapter mode.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.



### -param Mode [in]

A WINBIO_SENSOR_MODE value. This can be one of the following values: 

<ul>
<li>WINBIO_SENSOR_UNKNOWN_MODE</li>
<li>WINBIO_SENSOR_BASIC_MODE</li>
<li>WINBIO_SENSOR_ADVANCED_MODE</li>
<li>WINBIO_SENSOR_NAVIGATION_MODE</li>
<li>WINBIO_SENSOR_SLEEP_MODE</li>
</ul>

## -returns



If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

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
The <i>Pipeline</i> argument cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DEVICE_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was a hardware failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b> or the <b>SensorHandle</b> member is set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_SENSOR_MODE</b></dt>
</dl>
</td>
<td width="60%">
The sensor adapter does not support the value specified by the <i>Mode</i> parameter.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

