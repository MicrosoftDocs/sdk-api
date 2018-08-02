---
UID: NF:winddi.EngUnlockSurface
title: EngUnlockSurface function
author: windows-sdk-content
description: The EngUnlockSurface function causes GDI to unlock the surface.
old-location: display\engunlocksurface.htm
old-project: display
ms.assetid: 49d089e3-c900-4f81-a6ee-420a5558a4ff
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngUnlockSurface, EngUnlockSurface function [Display Devices], display.engunlocksurface, gdifncs_a7050a36-0beb-4f7e-857c-5d1e13d5f530.xml, winddi/EngUnlockSurface
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
 - EngUnlockSurface
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngUnlockSurface function


## -description


The <b>EngUnlockSurface</b> function causes GDI to unlock the surface.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the surface to be unlocked.


## -returns



None




## -remarks



The specified surface must previously have been locked by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564968">EngLockSurface</a>. The pointer to the SURFOBJ structure must not be used after this call.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564968">EngLockSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

