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

# PDD_WAITFORVERTICALBLANK callback function


## -description


The <b>DdWaitForVerticalBlank</b> callback function returns the vertical blank status of the device.


## -parameters




### -param Arg1








#### - lpWaitForVerticalBlank

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551765">DD_WAITFORVERTICALBLANKDATA</a> structure that contains the information required to obtain the vertical blank status.


## -returns



<b>DdWaitForVerticalBlank</b> returns one of the following callback codes:




## -remarks



Depending on the value of the <b>dwFlags</b> member of the DD_WAITFORVERTICALBLANKDATA structure at <i>lpWaitForVerticalBlank</i>, the driver should do the following:

<ul>
<li>
If <b>dwFlags</b> is DDWAITVB_I_TESTVB, the driver should query the current vertical blanking status. The driver should set the <b>bIsInVB</b> member of DD_WAITFORVERTICALBLANKDATA to <b>TRUE</b> if the monitor is currently in a vertical blank; otherwise the driver should set <b>bIsInVB</b> to <b>FALSE</b>.

</li>
<li>
If <b>dwFlags</b> is DDWAITVB_BLOCKBEGIN, the driver should block and wait until a vertical blank begins. If a vertical blank is in progress when the driver begins the block, the driver should wait until the next vertical blank begins before returning.

</li>
<li>
If <b>dwFlags</b> is DDWAITVB_BLOCKEND, the driver should block and wait until a vertical blank ends.

</li>
</ul>
When the driver successfully handles the action specified in <b>dwFlags</b>, it should set DD_OK in the <b>ddRVal</b> member of DD_WAITFORVERTICALBLANKDATA and return DDHAL_DRIVER_HANDLED. The driver should return DDHAL_DRIVER_NOTHANDLED for those flags that it is incapable of handling.

<b>DdWaitForVerticalBlank</b> allows an application to synchronize itself with the vertical blanking interval (VBI).

<div class="alert"><b>Note</b>  <b>DdWaitForVerticalBlank</b> should never enter a polling loop if the monitor power state will cause the driver to hang. For example, during a monitor power-down, an application might call <b>WaitForVerticalBlank</b>. The DirectDraw runtime calls the display driver's <b>DdWaitForVerticalBlank</b> entry point, which waits for the status to change. If the monitor is powered down, this value will never change--unless the driver writer prepares for this scenario. One solution is to include a time out in the polling loop while waiting for a vertical blank. The sample Permedia2 driver is simply set to not poll at all if the monitor is powered down. <p class="note">There is also an issue with the WHQL Display Compatibility Tests (DCTs). One of the DCTs for power management powers down the monitor and then polls the vertical blank status, waiting for it to change. If the driver always reports the same vertical blank status when the monitor is powered down, then the test application will hang waiting for the result to change. This was fixed in the Permedia2 sample driver by returning alternating results while the monitor is powered down. That is, the first time the driver's <b>DdWaitForVerticalBlank</b> entry point is called with the DDWAIT_I_TESTVB flag (when the monitor is powered down), it returns <b>FALSE</b>, the next time it returns <b>TRUE</b>, next time <b>FALSE</b>, etc.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551765">DD_WAITFORVERTICALBLANKDATA</a>
 

 

