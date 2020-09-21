---
UID: NF:winddi.EngBugCheckEx
title: EngBugCheckEx function (winddi.h)
description: The EngBugCheckEx function brings down the system in a controlled manner when the caller discovers an unrecoverable error that would corrupt the system if the caller continued to run.
helpviewer_keywords: ["EngBugCheckEx","EngBugCheckEx function [Display Devices]","display.engbugcheckex","gdifncs_0ed66a9e-1824-45cc-9237-ab0910e72915.xml","winddi/EngBugCheckEx"]
old-location: display\engbugcheckex.htm
tech.root: display
ms.assetid: 3b835719-cf11-4058-a557-c6618015f362
ms.date: 12/05/2018
ms.keywords: EngBugCheckEx, EngBugCheckEx function [Display Devices], display.engbugcheckex, gdifncs_0ed66a9e-1824-45cc-9237-ab0910e72915.xml, winddi/EngBugCheckEx
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Microsoft Windows Server 2003 and later.
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
 - EngBugCheckEx
 - winddi/EngBugCheckEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngBugCheckEx
---

# EngBugCheckEx function


## -description

The <b>EngBugCheckEx</b> function brings down the system in a controlled manner when the caller discovers an unrecoverable error that would corrupt the system if the caller continued to run.

## -parameters

### -param BugCheckCode [in]

Specifies a value that indicates the reason for the bug check.

### -param P1 [in]

Pointer to a value that supplies additional information, such as the address and data where a memory-corruption error occurred. The value depends on the value of the <i>BugCheckCode</i> parameter.

### -param P2 [in]

Pointer to a value that supplies additional information, such as the address and data where a memory-corruption error occurred. The value depends on the value of the <i>BugCheckCode</i> parameter.

### -param P3 [in]

Pointer to a value that supplies additional information, such as the address and data where a memory-corruption error occurred. The value depends on the value of the <i>BugCheckCode</i> parameter.

### -param P4 [in]

Pointer to a value that supplies additional information, such as the address and data where a memory-corruption error occurred. The value depends on the value of the <i>BugCheckCode</i> parameter.

## -returns

None

## -remarks

A bug check is a system-detected error that causes an immediate, controlled shutdown of the system. When a graphics driver discovers an unrecoverable error, it should generate a bug check.

A graphics driver should call <b>EngBugCheckEx </b><i>only</i> in the event of a fatal, unrecoverable error that could corrupt the system. Whenever possible, all graphics drivers should log an error and continue to run. For example, if a driver is unable to allocate required resources, it should log an error so that the system continues to run; it must not generate a bug check.

<b>EngBugCheckEx</b> can be useful in the early stages of developing a graphics driver, or while it is undergoing testing. In these circumstances, the <i>BugCheckCode</i> value passed to this function should be distinct from those codes already in use by Windows or its drivers. For a list of these codes, see <a href="/windows-hardware/drivers/debugger/bug-check-code-reference2">Bug Check Codes</a>.

However, even during driver development, this routine is of only limited use, because it results in a complete system shutdown. A more effective debugging method is to attach a kernel debugger to the system and then use routines that send messages to the debugger or break into the debugger. For more information, see <a href="/windows-hardware/drivers/devtest/using-debugging-code-in-a-driver">Using Debugging Code in a Driver</a>.