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

# DrvGetModes function


## -description


The <b>DrvGetModes</b> function lists the modes supported by a given device.


## -parameters




### -param hDriver [in]

Handle to the driver for which the modes must be enumerated. This is the handle passed in the <i>hDriver</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> function.


### -param cjSize

Specifies the size in bytes of the buffer pointed to by <i>pdm</i>.


### -param pdm [out, optional]

Pointer to the buffer containing <a href="https://msdn.microsoft.com/library/windows/hardware/ff552837">DEVMODEW</a> structure(s) for the driver to fill in, or <b>NULL</b>.


## -returns



The driver should return the number of bytes written to the buffer if <i>pdm</i> is not <b>NULL</b>. If <i>pdm</i>is <b>NULL</b>, the driver should return the number of bytes required to hold all mode data. The driver should return zero if an error occurs.




## -remarks



This function must be implemented in all display drivers.

Window Manager dynamically loads all display drivers associated with a miniport driver (based on the <b>InstalledDisplayDrivers</b> key in the registry). Each display driver is called to retrieve the list of modes supported by that combination of loaded drivers. For example, the VGA64K display driver only returns the 64K color modes that were returned in the list of modes obtained from the miniport driver.

<b>DrvGetModes</b> can be called before there is an active PDEV.

Refer to the <i>Permedia</i> samples to see a working implementation of <b>DrvGetModes</b>.

<div class="alert"><b>Note</b>    The Microsoft Windows Driver Kit (WDK) does not contain the 3Dlabs Permedia2 (<i>3dlabs.htm</i> ) and 3Dlabs Permedia3 (<i>Perm3.htm</i>) sample display drivers. You can get these sample drivers from the Windows Server 2003 SP1 Driver Development Kit (DDK), which you can download from the <a href="http://go.microsoft.com/fwlink/p/?linkid=21859">DDK - Windows Driver Development Kit</a> page of the WDHC website.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552837">DEVMODEW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564838">EngDeviceIoControl</a>
 

 

