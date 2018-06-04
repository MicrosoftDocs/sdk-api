---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# EngRestoreFloatingPointState function


## -description


The <b>EngRestoreFloatingPointState</b> function restores the Windows 2000 (and later) kernel floating-point state after the driver uses any floating-point or MMX hardware instructions.


## -parameters




### -param pBuffer [in]

Pointer to the buffer whose contents were filled by <a href="https://msdn.microsoft.com/library/windows/hardware/ff565010">EngSaveFloatingPointState</a>.


## -returns



<b>EngRestoreFloatingPointState</b> returns <b>TRUE</b> if successful. Otherwise, it returns <b>FALSE</b>.




## -remarks



The driver must save the current kernel floating-point state before using floating-point hardware instructions. On Intel architecture systems, this permits the use of MMX instructions if they are supported by the processor. Drivers that do not properly use <b>EngSaveFloatingPointState</b> and <b>EngRestoreFloatingPointState</b> when using floating-point or MMX hardware will cause random floating-point or MMX corruption in the calling application.

On every call to the driver, the driver must call <b>EngSaveFloatingPointState</b> once to preserve kernel state before using floating-point or MMX operations. It must also call <b>EngRestoreFloatingPointState</b> once after all floating-point or MMX operations are complete to reset the kernel state.

GDI automatically saves the floating-point state for any calls to a driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a> routine when the escape is OPENGL_CMD, OPENGL_GETINFO, or MCDFUNCS.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565010">EngSaveFloatingPointState</a>
 

 

