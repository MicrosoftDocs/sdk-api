---
UID: NF:winddi.EngDebugPrint
title: EngDebugPrint function (winddi.h)
description: The EngDebugPrint function prints the specified debug message to the kernel debugger.
helpviewer_keywords: ["EngDebugPrint","EngDebugPrint function [Display Devices]","display.engdebugprint","gdifncs_e3529861-721f-41f3-aedc-12ef88353b24.xml","winddi/EngDebugPrint"]
old-location: display\engdebugprint.htm
tech.root: display
ms.assetid: 2480adec-68b6-4ffe-8b20-2ca7cb1a4d79
ms.date: 12/05/2018
ms.keywords: EngDebugPrint, EngDebugPrint function [Display Devices], display.engdebugprint, gdifncs_e3529861-721f-41f3-aedc-12ef88353b24.xml, winddi/EngDebugPrint
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngDebugPrint
 - winddi/EngDebugPrint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngDebugPrint
---

# EngDebugPrint function


## -description

The <b>EngDebugPrint</b> function prints the specified debug message to the kernel debugger.

## -parameters

### -param StandardPrefix [in]

Pointer to a string that is prepended to <i>DebugMessage</i>.

### -param DebugMessage [in]

Pointer to a string containing the debug message to be printed.

### -param ap [in]

Specifies the variable argument list.

## -returns

None

## -remarks

<b>EngDebugPrint</b> is useful for debugging drivers that are under development. It prints <i>StandardPrefix</i>, followed by <i>DebugMessage</i>, to the kernel debugger.

The <i>StandardPrefix</i> parameter acts as a unique identifier of the driver executing the debug statement; therefore, the same string should be used for all calls to <b>EngDebugPrint</b> by a single driver.

The <i>DebugMessage</i> parameter is a variable argument ASCII C string; that is, it can contain both ordinary characters and C-style conversion specifications. The argument list contained in <i>ap</i> can have any number of arguments of any type in it.

An example use of <b>EngDebugPrint</b> follows:


```
#define STANDARD_DEBUG_PREFIX     "Permedia: "
LONG bank;
LONG width;
...
VOID MyDebugPrint(PCHAR DebugMessage, ...)
{
    va_list ap;

    va_start(ap, DebugMessage);
    EngDebugPrint(STANDARD_DEBUG_PREFIX, DebugMessage, ap);
    va_end(ap);
}
...
MyDebugPrint("Bank: %lx; Width: %ld", bank, width);
```


<div class="alert"><b>Note</b>    The Microsoft Windows Driver Kit (WDK) does not contain the Permedia (<i>3dlabs.htm</i> and <i>Perm3.htm</i>) and FrameBuffer (<i>Framebuf.htm) </i> sample display drivers. You can get these sample drivers from the Windows Server 2003 SP1 Driver Development Kit (DDK), which you can download from the <a href="/windows-hardware/drivers/devtest/">DDK - Windows Driver Development Kit</a> page of the WDHC website.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engdebugbreak">EngDebugBreak</a>