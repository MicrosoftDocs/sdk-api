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

# _SP_DETECTDEVICE_PARAMS structure


## -description


An SP_DETECTDEVICE_PARAMS structure corresponds to a DIF_DETECT installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the size of the header and the DIF code for the request. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>. 


### -field DetectProgressNotify

A callback routine that displays a progress bar for the device detection operation. The callback routine is supplied by the <a href="devinst.device_installation_components">device installation component</a> that sends the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543674">DIF_DETECT</a> request. The callback has the following prototype:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef BOOL (CALLBACK* PDETECT_PROGRESS_NOTIFY)(
    IN PVOID ProgressNotifyParam,
    IN DWORD DetectComplete
    );</pre>
</td>
</tr>
</table></span></div>
<i>ProgressNotifyParam</i> is an opaque "handle" that identifies the detection operation. This value is supplied by the <a href="devinst.device_installation_components">device installation component</a> that sent the DIF_DETECT request. 

<i>DetectComplete</i> is a value between 0 and 100 that indicates the percent completion. The class installer increments this value at various stages of its detection activities, to notify the user of its progress.


### -field ProgressNotifyParam

The opaque <b>ProgressNotifyParam</b> "handle" that the class installer passes to the progress callback routine.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543674">DIF_DETECT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

