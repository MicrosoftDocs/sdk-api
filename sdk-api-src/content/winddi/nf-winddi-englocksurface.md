---
UID: NF:winddi.EngLockSurface
title: EngLockSurface function
author: windows-sdk-content
description: The EngLockSurface function creates a user object for a given surface. This function gives drivers access to surfaces they create.
old-location: display\englocksurface.htm
tech.root: display
ms.assetid: a5d44e16-459c-4722-b3e8-5dc4b5be5865
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EngLockSurface, EngLockSurface function [Display Devices], display.englocksurface, gdifncs_99ca0d6a-a445-42ad-96fb-4ef8d3e23db7.xml, winddi/EngLockSurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngLockSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngLockSurface function


## -description


The <b>EngLockSurface</b> function creates a user object for a given surface. This function gives drivers access to surfaces they create.


## -parameters




### -param hsurf

Handle to the surface to be locked.


## -returns



<b>EngLockSurface</b> returns a pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure if the function is successful. Otherwise, this function returns <b>NULL</b>.




## -remarks



This function gives drivers access to surfaces they create.

The driver is responsible for unlocking the surface when it no longer needs it. Surfaces should be locked only for very short periods of time.

Use the <a href="https://msdn.microsoft.com/49d089e3-c900-4f81-a6ee-420a5558a4ff">EngUnlockSurface</a> function to unlock the surface.




## -see-also




<a href="https://msdn.microsoft.com/49d089e3-c900-4f81-a6ee-420a5558a4ff">EngUnlockSurface</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

