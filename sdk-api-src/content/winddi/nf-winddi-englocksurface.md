---
UID: NF:winddi.EngLockSurface
title: EngLockSurface function
author: windows-sdk-content
description: The EngLockSurface function creates a user object for a given surface. This function gives drivers access to surfaces they create.
old-location: display\englocksurface.htm
old-project: display
ms.assetid: a5d44e16-459c-4722-b3e8-5dc4b5be5865
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngLockSurface, EngLockSurface function [Display Devices], display.englocksurface, gdifncs_99ca0d6a-a445-42ad-96fb-4ef8d3e23db7.xml, winddi/EngLockSurface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngLockSurface function


## -description


The <b>EngLockSurface</b> function creates a user object for a given surface. This function gives drivers access to surfaces they create.


## -parameters




### -param hsurf

Handle to the surface to be locked.


## -returns



<b>EngLockSurface</b> returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure if the function is successful. Otherwise, this function returns <b>NULL</b>.




## -remarks



This function gives drivers access to surfaces they create.

The driver is responsible for unlocking the surface when it no longer needs it. Surfaces should be locked only for very short periods of time.

Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565422">EngUnlockSurface</a> function to unlock the surface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565422">EngUnlockSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

