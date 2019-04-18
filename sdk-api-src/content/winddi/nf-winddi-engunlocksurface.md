---
UID: NF:winddi.EngUnlockSurface
title: EngUnlockSurface function (winddi.h)
author: windows-sdk-content
description: The EngUnlockSurface function causes GDI to unlock the surface.
old-location: display\engunlocksurface.htm
tech.root: display
ms.assetid: 49d089e3-c900-4f81-a6ee-420a5558a4ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngUnlockSurface, EngUnlockSurface function [Display Devices], display.engunlocksurface, gdifncs_a7050a36-0beb-4f7e-857c-5d1e13d5f530.xml, winddi/EngUnlockSurface
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
 - EngUnlockSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngUnlockSurface function


## -description


The <b>EngUnlockSurface</b> function causes GDI to unlock the surface.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface to be unlocked.


## -returns



None




## -remarks



The specified surface must previously have been locked by a call to <a href="https://msdn.microsoft.com/a5d44e16-459c-4722-b3e8-5dc4b5be5865">EngLockSurface</a>. The pointer to the SURFOBJ structure must not be used after this call.




## -see-also




<a href="https://msdn.microsoft.com/a5d44e16-459c-4722-b3e8-5dc4b5be5865">EngLockSurface</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

