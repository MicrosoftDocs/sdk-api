---
UID: NF:winddi.EngRestoreFloatingPointState
title: EngRestoreFloatingPointState function (winddi.h)
author: windows-sdk-content
description: The EngRestoreFloatingPointState function restores the Windows 2000 (and later) kernel floating-point state after the driver uses any floating-point or MMX hardware instructions.
old-location: display\engrestorefloatingpointstate.htm
tech.root: display
ms.assetid: afdf7ce8-a053-424d-8b3e-0e7bc391ecb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngRestoreFloatingPointState, EngRestoreFloatingPointState function [Display Devices], display.engrestorefloatingpointstate, gdifncs_e3f3f96d-5e04-4c8c-b22b-73df32e862e2.xml, winddi/EngRestoreFloatingPointState
ms.topic: function
f1_keywords: 
 - "winddi/EngRestoreFloatingPointState"
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
 - EngRestoreFloatingPointState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngRestoreFloatingPointState function


## -description


The <b>EngRestoreFloatingPointState</b> function restores the Windows 2000 (and later) kernel floating-point state after the driver uses any floating-point or MMX hardware instructions.


## -parameters




### -param pBuffer [in]

Pointer to the buffer whose contents were filled by <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engsavefloatingpointstate">EngSaveFloatingPointState</a>.


## -returns



<b>EngRestoreFloatingPointState</b> returns <b>TRUE</b> if successful. Otherwise, it returns <b>FALSE</b>.




## -remarks



The driver must save the current kernel floating-point state before using floating-point hardware instructions. On Intel architecture systems, this permits the use of MMX instructions if they are supported by the processor. Drivers that do not properly use <b>EngSaveFloatingPointState</b> and <b>EngRestoreFloatingPointState</b> when using floating-point or MMX hardware will cause random floating-point or MMX corruption in the calling application.

On every call to the driver, the driver must call <b>EngSaveFloatingPointState</b> once to preserve kernel state before using floating-point or MMX operations. It must also call <b>EngRestoreFloatingPointState</b> once after all floating-point or MMX operations are complete to reset the kernel state.

GDI automatically saves the floating-point state for any calls to a driver's <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a> routine when the escape is OPENGL_CMD, OPENGL_GETINFO, or MCDFUNCS.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvescape">DrvEscape</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engsavefloatingpointstate">EngSaveFloatingPointState</a>
 

 

