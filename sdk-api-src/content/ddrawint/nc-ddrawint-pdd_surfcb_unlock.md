---
UID: NC:ddrawint.PDD_SURFCB_UNLOCK
title: PDD_SURFCB_UNLOCK
author: windows-driver-content
description: The DdUnLock callback function releases the lock held on the specified surface.
old-location: display\ddunlock.htm
old-project: display
ms.assetid: dbb7b34c-5473-42b9-b16f-e71b9c3e1db8
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DdUnlock, DdUnlock callback function [Display Devices], PDD_SURFCB_UNLOCK, PDD_SURFCB_UNLOCK callback, ddfncs_9599bb87-0f48-4481-a5c8-4c3d60dc1fc6.xml, ddrawint/DdUnlock, display.ddunlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddrawint.h
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddrawint.h
api_name:
-	DdUnlock
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_SURFCB_UNLOCK callback function


## -description


The <i>DdUnLock</i> callback function releases the lock held on the specified surface.


## -parameters




### -param Arg1








#### - lpUnlock

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551745">DD_UNLOCKDATA</a> structure that contains the information required to perform the lock release.


## -returns



<i>DdUnLock</i> returns one of the following callback codes:




## -remarks



The driver does not need to verify that the memory was previously locked down by <a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a>, because DirectDraw does parameter validation before calling this routine. 

<i>DdUnLock</i> can be called with a disabled <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. A PDEV is disabled or enabled by calling the display driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a> function. See <a href="https://msdn.microsoft.com/f7badbe8-b24f-438a-8937-95bb98de6310">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551745">DD_UNLOCKDATA</a>



<a href="https://msdn.microsoft.com/b5256ed8-79be-4c7b-a079-ed3bca954e9e">DdLock</a>
 

 

