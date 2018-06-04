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

# PIBIO_STORAGE_NOTIFY_POWER_CHANGE_FN callback function


## -description


Called by the Windows Biometric Framework when the system is ready to enter a low-power state or when the system 
    has been awakened from a low-power state. The purpose of this function is to enable the adapter to respond to 
    transitions in the computer power state.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure 
      associated with the biometric unit performing the operation.


### -param PowerEventType [in]

Indicates the nature of the change. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PBT_APMSUSPEND"></a><a id="pbt_apmsuspend"></a><dl>
<dt><b>PBT_APMSUSPEND</b></dt>
</dl>
</td>
<td width="60%">
The system is entering a low-power state

</td>
</tr>
<tr>
<td width="40%"><a id="PBT_APMRESUMEAUTOMATIC"></a><a id="pbt_apmresumeautomatic"></a><dl>
<dt><b>PBT_APMRESUMEAUTOMATIC</b></dt>
</dl>
</td>
<td width="60%">
The system is returning from a low-power state.

</td>
</tr>
<tr>
<td width="40%"><a id="PBT_APMPOWERSTATUSCHANGE"></a><a id="pbt_apmpowerstatuschange"></a><dl>
<dt><b>PBT_APMPOWERSTATUSCHANGE</b></dt>
</dl>
</td>
<td width="60%">
The status of the system's power source is changing (e.g., the system has switched from battery to line 
        power, or the battery is getting low).

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an 
       <b>HRESULT</b> value that indicates the error. Possible values include, but are not 
       limited to, those in the following table.  For a list of common error codes, see 
       <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
The <i>Pipeline</i> argument was <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>PowerEventType</i> argument was not one of the values listed in the table.

</td>
</tr>
</table>
 




## -remarks



When it receives a 
    <a href="https://msdn.microsoft.com/dc56fee3-e0df-4f8e-8a41-92460279280a">PBT_APMPOWERSTATUSCHANGE</a> event, the adapter 
     should call the Microsoft Win32 
     <a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a> API to 
     determine the new power status.

The biometric framework calls this adapter entry point asynchronously, in the context of an arbitrary thread. 
     It is the adapter's responsibility to synchronize the processing of this call with any other work it may be 
     doing.




## -see-also




<a href="https://msdn.microsoft.com/6d440ef2-2b9d-4f7a-a445-2420f07f3784">GetSystemPowerStatus</a>



<a href="https://msdn.microsoft.com/dc56fee3-e0df-4f8e-8a41-92460279280a">PBT_APMPOWERSTATUSCHANGE</a>
 

 

