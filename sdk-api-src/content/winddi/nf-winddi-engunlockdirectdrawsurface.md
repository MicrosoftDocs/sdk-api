---
UID: NF:winddi.EngUnlockDirectDrawSurface
title: EngUnlockDirectDrawSurface function
author: windows-driver-content
description: The EngUnlockDirectDrawSurface function releases the lock on the specified surface.
old-location: display\engunlockdirectdrawsurface.htm
old-project: display
ms.assetid: 61d1ff1a-d5e3-4542-953c-8b1771622a63
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: EngUnlockDirectDrawSurface, EngUnlockDirectDrawSurface function [Display Devices], display.engunlockdirectdrawsurface, gdifncs_6582e033-3e56-4a8d-904d-2978c63ddd4b.xml, winddi/EngUnlockDirectDrawSurface
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngUnlockDirectDrawSurface
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngUnlockDirectDrawSurface function


## -description


The <b>EngUnlockDirectDrawSurface</b> function releases the lock on the specified surface.


## -parameters




### -param pSurface [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface to be unlocked.


## -returns



<b>EngUnlockDirectDrawSurface</b> returns <b>TRUE</b> when it successfully unlocks the specified surface. Otherwise, it returns <b>FALSE</b>.




## -remarks



The surface must previously have been locked by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564966">EngLockDirectDrawSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564966">EngLockDirectDrawSurface</a>
 

 

