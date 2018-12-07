---
UID: NC:winbio_adapter.PIBIO_SENSOR_NOTIFY_POWER_CHANGE_FN
title: PIBIO_SENSOR_NOTIFY_POWER_CHANGE_FN
author: windows-sdk-content
description: Receives notification about a change in the computer power state and prepares the sensor adapter accordingly.
old-location: secbiomet\sensoradapternotifypowerchange.htm
tech.root: SecBioMet
ms.assetid: 7EA9D7E7-3DB9-4131-A747-B0388310ACB5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PBT_APMPOWERSTATUSCHANGE, PBT_APMRESUMEAUTOMATIC, PBT_APMSUSPEND, PIBIO_SENSOR_NOTIFY_POWER_CHANGE_FN, PIBIO_SENSOR_NOTIFY_POWER_CHANGE_FN callback, SensorAdapterNotifyPowerChange, SensorAdapterNotifyPowerChange callback function [Windows Biometric Framework API], secbiomet.sensoradapternotifypowerchange, winbio_adapter/SensorAdapterNotifyPowerChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - SensorAdapterNotifyPowerChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_SENSOR_NOTIFY_POWER_CHANGE_FN callback function


## -description


Called by the Windows Biometric Framework when the system is ready to enter a low-power state or when the system has been awakened from a low-power state. The purpose of this function is to enable the adapter to respond to transitions in the computer power state.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation


### -param PowerEventType [in]

Indicates the nature of the change. It can be one of the following values:



#### PBT_APMSUSPEND (The system is entering a low-power state)



##### )



####### )


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
The <i>Pipeline</i> argument was NULL

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>PowerEventType</i> argument was not one of the values listed.

</td>
</tr>
</table>
 




## -remarks



When it receives a <a href="https://msdn.microsoft.com/dc56fee3-e0df-4f8e-8a41-92460279280a">PBT_APMPOWERSTATUSCHANGE</a> event, the adapter should call the Microsoft Win32<a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a>API to determine the new power status.

The biometric framework calls this adapter entry point asynchronously, in the context of an arbitrary thread. It is the adapter's responsibility to synchronize the processing of this call with any other work it may be doing.



