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

<b>EngBugCheckEx</b> can be useful in the early stages of developing a graphics driver, or while it is undergoing testing. In these circumstances, the <i>BugCheckCode</i> value passed to this function should be distinct from those codes already in use by Windows or its drivers. For a list of these codes, see <a href="https://msdn.microsoft.com/DBA85578-97CF-4BD7-A67D-1C7AD2E9B2BB">Bug Check Codes</a>.

However, even during driver development, this routine is of only limited use, because it results in a complete system shutdown. A more effective debugging method is to attach a kernel debugger to the system and then use routines that send messages to the debugger or break into the debugger. For more information, see <a href="https://msdn.microsoft.com/6ed74bcc-290c-44e3-943e-4169527dfa18">Using Debugging Code in a Driver</a>.



