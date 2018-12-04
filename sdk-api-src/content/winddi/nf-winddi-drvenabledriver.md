---
UID: NF:winddi.DrvEnableDriver
title: DrvEnableDriver function
author: windows-sdk-content
description: The DrvEnableDriver function is the initial driver entry point exported by the driver DLL.
old-location: display\drvenabledriver.htm
tech.root: display
ms.assetid: b7aa5442-bbf5-4f9e-ad39-bf8a2d01c50e
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: DrvEnableDriver, DrvEnableDriver function [Display Devices], ddifncs_ceb25289-afd3-447e-85e7-d89fa95aebd4.xml, display.drvenabledriver, winddi/DrvEnableDriver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvEnableDriver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvEnableDriver function


## -description


The <b>DrvEnableDriver</b> function is the initial driver entry point exported by the driver DLL. It fills in a <a href="https://msdn.microsoft.com/dbeaecf8-dea1-4412-babb-6e40bf5dc7b0">DRVENABLEDATA</a> structure with the driver's graphics DDI version number and the calling addresses of all graphics DDI functions supported by the driver.


## -parameters




### -param iEngineVersion

Identifies the version of GDI that is currently running.


### -param cj

Is the size in bytes of the structure pointed to by <i>pded</i>. If the structure is larger than expected, extra members should be left unmodified.


### -param pded [in]

Pointer to a <a href="https://msdn.microsoft.com/dbeaecf8-dea1-4412-babb-6e40bf5dc7b0">DRVENABLEDATA</a> structure. GDI zero-initializes <i>cj</i> bytes before the call. The driver fills in its own data.


## -returns



The return value is <b>TRUE</b> if the specified driver is enabled. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



<b>DrvEnableDriver</b> must be implemented in all graphics drivers. If you use the Windows Driver Kit (WDK) build tools and have set TARGETTYPE to GDI_DRIVER (see <a href="https://msdn.microsoft.com/bec1e9cc-a846-43e5-bc9e-e43a151ef6c4">Building a Printer Graphics DLL</a>), this function must be named <b>DrvEnableDriver</b>. This is the only display driver function that must be accessed by name. All other display driver functions are accessed through function pointers; therefore, their names are presented in this documentation as pseudonames. 

One-time initializations, such as allocating semaphores, can also be performed by this function. The driver should wait until <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a> is called before enabling hardware, such as a display.

When performing version checking using the value provided in <i>iEngineVersion</i>, the driver should use the appropriate DDI_DRIVER_VERSION_<i>Xxx</i> constant (defined in <i>winddi.h</i>) shown in the following table. Drivers should almost never check just for equality since new versions and service pack releases for the operating system will be released in the future. For more information, see <a href="https://msdn.microsoft.com/dbeaecf8-dea1-4412-babb-6e40bf5dc7b0">DRVENABLEDATA</a>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/dbeaecf8-dea1-4412-babb-6e40bf5dc7b0">DRVENABLEDATA</a>



<a href="https://msdn.microsoft.com/2ff20004-ec2e-4192-a5f1-e3e9d2bfad3c">DRVFN</a>



<a href="https://msdn.microsoft.com/8f12cc40-6cff-4e40-a264-58d16d3e55bd">DrvDisableDriver</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>
 

 

