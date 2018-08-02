---
UID: NF:winddi.EngLockDirectDrawSurface
title: EngLockDirectDrawSurface function
author: windows-sdk-content
description: The EngLockDirectDrawSurface function locks the kernel-mode handle of a DirectDraw surface.
old-location: display\englockdirectdrawsurface.htm
old-project: display
ms.assetid: be43afe9-97c9-4ae4-b18c-3312ae757798
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngLockDirectDrawSurface, EngLockDirectDrawSurface function [Display Devices], display.englockdirectdrawsurface, gdifncs_f0027001-42bd-4f64-b5c0-c7ec3768f72c.xml, winddi/EngLockDirectDrawSurface
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
 - EngLockDirectDrawSurface
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngLockDirectDrawSurface function


## -description


The <b>EngLockDirectDrawSurface</b> function locks the kernel-mode handle of a DirectDraw surface.


## -parameters




### -param hSurface [in]

Handle to the surface to be locked.


## -returns



<b>EngLockDirectDrawSurface</b> returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface information upon success. Otherwise, it returns a <b>NULL</b> pointer.




## -remarks



<b>EngLockDirectDrawSurface</b> allows driver writers to lock DirectDraw surfaces. Locking the handle guarantees synchronized behavior and preserves the handle from being deleted by other threads in the system.

Currently, the driver receives DirectDraw surface handles only from the Direct3D texturing interface. Consequently, only drivers that perform texturing need to lock texture surfaces.

Upon completion of texturing, the driver must release the locked handle by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff565042">EngUnlockDirectDrawSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565042">EngUnlockDirectDrawSurface</a>
 

 

