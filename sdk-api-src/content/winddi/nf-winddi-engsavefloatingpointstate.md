---
UID: NF:winddi.EngSaveFloatingPointState
title: EngSaveFloatingPointState function
author: windows-driver-content
description: The EngSaveFloatingPointState function saves the current Windows 2000 (and later) kernel floating-point state.
old-location: display\engsavefloatingpointstate.htm
old-project: display
ms.assetid: 25e9ae3b-a3a5-438c-84e0-53f2be7ba29c
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: EngSaveFloatingPointState, EngSaveFloatingPointState function [Display Devices], display.engsavefloatingpointstate, gdifncs_624220d2-de91-4558-86aa-94db622660eb.xml, winddi/EngSaveFloatingPointState
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
-	EngSaveFloatingPointState
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngSaveFloatingPointState function


## -description


The <b>EngSaveFloatingPointState</b> function saves the current Windows 2000 (and later) kernel floating-point state.


## -parameters




### -param pBuffer

Pointer to the buffer that receives the floating-point state. This buffer must be zero-initialized, and must be in nonpaged memory.


### -param cjBufferSize [in, out]

Specifies the size, in bytes, of the buffer to which <i>pBuffer</i> points.


## -returns



If <i>pBuffer</i> is non-<b>NULL</b>, <b>EngSaveFloatingPointState</b> returns <b>TRUE</b> if the state is successfully saved. It returns <b>FALSE</b> if the specified buffer is too small or the state cannot be saved.

If <i>pBuffer</i> is <b>NULL</b> or <i>cjBufferSize</i> is zero, <b>EngSaveFloatingPointState</b> returns the size of the buffer needed to save the floating-point state. If the return value is zero, the processor does not have hardware floating-point capability. In this case, the driver must not use any floating-point instructions.




## -remarks



The driver must save the current kernel floating-point state before using floating-point hardware instructions. On Intel architecture systems, this permits the use of MMX instructions if they are supported by the processor. Drivers that do not properly use <b>EngSaveFloatingPointState</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff565006">EngRestoreFloatingPointState</a> when using floating-point or MMX hardware will cause random floating-point or MMX corruption in the calling application.

On every call to the driver, the driver must call <b>EngSaveFloatingPointState</b> once to preserve kernel state before using floating-point or MMX operations. It must also call <b>EngRestoreFloatingPointState</b> once after all floating-point or MMX operations are complete to reset the kernel state.

GDI automatically saves the floating-point state for any calls to a driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a> routine when the escape is OPENGL_CMD, OPENGL_GETINFO, or MCDFUNCS.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565006">EngRestoreFloatingPointState</a>
 

 

