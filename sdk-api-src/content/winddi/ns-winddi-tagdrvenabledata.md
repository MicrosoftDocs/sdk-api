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

# tagDRVENABLEDATA structure


## -description


The DRVENABLEDATA structure contains a pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556221">DRVFN</a> structures and the graphics DDI version number of an NT-based operating system.


## -struct-fields




### -field iDriverVersion

Specifies the graphics DDI version number of the NT-based operating system that the driver is targeted for. This member can be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Operating System Version</th>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT4

</td>
<td>
Windows NT 4.0

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_SP3

</td>
<td>
Windows NT 4.0 Service Pack 3

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT5

</td>
<td>
Windows 2000

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT5_01

</td>
<td>
Windows XP

</td>
</tr>
<tr>
<td>
DDI_DRIVER_VERSION_NT5_01_SP1

</td>
<td>
Windows XP Service Pack 1

</td>
</tr>
</table>
 

See the Remarks section for more information.


### -field c

Specifies the number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556221">DRVFN</a> structures in the buffer pointed to by the <b>pdrvfn</b> member.


### -field pdrvfn

Pointer to a buffer containing an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556221">DRVFN</a> structures.


## -remarks



To run on these NT-based operating systems versions, the <b>iDriverVersion</b> member must be set as follows:

<table>
<tr>
<th>Windows version</th>
<th>Value of iDriverVersion</th>
</tr>
<tr>
<td>
Windows NT 4.0

</td>
<td>
<b>iDriverVersion</b> == DDI_DRIVER_VERSION_NT4

</td>
</tr>
<tr>
<td>
Windows NT 4.0 SP3

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_SP3

</td>
</tr>
<tr>
<td>
Windows 2000

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_NT5

</td>
</tr>
<tr>
<td>
Windows XP

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_NT5_01

</td>
</tr>
<tr>
<td>
Windows XP SP1

</td>
<td>
DDI_DRIVER_VERSION_NT4 &lt;= <b>iDriverVersion</b> &lt;= DDI_DRIVER_VERSION_NT5_01_SP1

</td>
</tr>
</table>
 

As the table shows, a driver can run on any of these operating system versions if <b>iDriverVersion</b> is set to DDI_DRIVER_VERSION_NT4, but a driver can run only on Windows XP and later versions of the operating system if <b>iDriverVersion</b> is set to DDI_DRIVER_VERSION_NT5_01.

<div class="alert"><b>Note</b>  
     If a driver implements a <i>DrvXxx</i> graphics DDI that is not supported in all versions of Windows, the driver cannot specify a DRVFN entry for that graphics DDI when running on versions of Windows that do not support it. If the driver does specify a DRVFN entry for such a graphics DDI, Windows will reject the driver. The <i>permedia2</i> sample demonstrates how to specify different DRVFN structures for different versions of Windows.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556221">DRVFN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556210">DrvEnableDriver</a>
 

 

