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

# BatteryClassQueryWmiDataBlock function


## -description


The <b>BatteryClassQueryWmiDataBlock</b> routine is used by battery miniclass drivers inside their <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routines to allow the battery class driver to process the WMI data block query requests it handles on behalf of the driver.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle that was previously received from <a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a>.


### -param DeviceObject [in, out]

Pointer to the driver's device object.  The battery miniclass driver should pass the matching parameter it receives as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine.


### -param Irp [in, out]

Pointer to the WMI query data block request.  The battery miniclass driver should pass the matching parameter it receives as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine.


### -param GuidIndex [in]

Specifies the WMI class by its index.  The battery miniclass driver should pass the matching parameter it receives as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine.


### -param InstanceLengthArray [out]

Pointer to an array of ULONG values that indicate the length of each instance to be returned.  The battery miniclass driver should pass the matching parameter it receives as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine.


### -param OutBufferSize [in]

Specifies the maximum number of bytes available to receive data in the buffer specified by the <i>Buffer</i> parameter.  The battery miniclass driver should pass the value of the <i>BufferAvail</i> parameter it receives as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine.


### -param Buffer [out, optional]

Pointer to the buffer to receive the instance data.  If the buffer is too small to hold the data, <b>BatteryClassQueryWmiDataBlock</b> returns a status value of STATUS_BUFFER_TOO_SMALL.  The battery miniclass driver should pass the matching parameter it receives as input to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine.


## -returns



<b>BatteryClassQueryWmiDataBlock</b> returns an NT status code.  Possible return values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The battery class driver successfully handled the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The battery class driver cannot handle the request because the buffer specified by the <i>Buffer</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_WMI_GUID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The battery class driver does not handle this WMI class.

</td>
</tr>
</table>
 




## -remarks



By design, a battery miniclass driver should call <b>BatteryClassQueryWmiDataBlock</b> inside its <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine before processing the request.  The miniclass driver should pass the parameters it receives as input to its <b>DpWmiQueryDataBlock</b> routine.  If the battery class driver returns any status other than STATUS_WMI_GUID_NOT_FOUND, the routine has handled the request on behalf of the miniclass driver.  In that case, the class driver has already called <a href="https://msdn.microsoft.com/library/windows/hardware/ff565798">WmiCompleteRequest</a>, and miniclass driver must not call it again. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536270">BatteryClassSystemControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565798">WmiCompleteRequest</a>
 

 

