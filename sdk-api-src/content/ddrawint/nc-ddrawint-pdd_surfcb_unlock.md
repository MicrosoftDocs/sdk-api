---
UID: NC:ddrawint.PDD_SURFCB_UNLOCK
title: PDD_SURFCB_UNLOCK (ddrawint.h)
description: The DdUnLock callback function releases the lock held on the specified surface.
old-location: display\ddunlock.htm
tech.root: display
ms.assetid: dbb7b34c-5473-42b9-b16f-e71b9c3e1db8
ms.date: 12/05/2018
ms.keywords: DdUnlock, DdUnlock callback function [Display Devices], PDD_SURFCB_UNLOCK, PDD_SURFCB_UNLOCK callback, ddfncs_9599bb87-0f48-4481-a5c8-4c3d60dc1fc6.xml, ddrawint/DdUnlock, display.ddunlock
ms.topic: callback
f1_keywords:
- ddrawint/DdUnlock
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- ddrawint.h
api_name:
- DdUnlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_SURFCB_UNLOCK callback function


## -description


The <i>DdUnLock</i> callback function releases the lock held on the specified surface.


## -parameters




### -param Arg1








#### - lpUnlock

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_unlockdata">DD_UNLOCKDATA</a> structure that contains the information required to perform the lock release.


## -returns



<i>DdUnLock</i> returns one of the following callback codes:




## -remarks



The driver does not need to verify that the memory was previously locked down by <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a>, because DirectDraw does parameter validation before calling this routine. 

<i>DdUnLock</i> can be called with a disabled <a href="https://docs.microsoft.com/windows-hardware/drivers/">PDEV</a>. A PDEV is disabled or enabled by calling the display driver's <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a> function. See <a href="https://docs.microsoft.com/windows-hardware/drivers/display/managing-pdevs">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_unlockdata">DD_UNLOCKDATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a>
 

 

