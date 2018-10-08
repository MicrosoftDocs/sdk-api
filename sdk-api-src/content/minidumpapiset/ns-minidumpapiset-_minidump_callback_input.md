---
UID: NS:minidumpapiset._MINIDUMP_CALLBACK_INPUT
title: "_MINIDUMP_CALLBACK_INPUT"
author: windows-sdk-content
description: Contains information used by the MiniDumpCallback function.
old-location: base\minidump_callback_input_str.htm
tech.root: debug
ms.assetid: 0ce3083c-21c9-48a4-9099-1dab31afcafa
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: "*PMINIDUMP_CALLBACK_INPUT, MINIDUMP_CALLBACK_INPUT, MINIDUMP_CALLBACK_INPUT structure, PMINIDUMP_CALLBACK_INPUT, PMINIDUMP_CALLBACK_INPUT structure pointer, _MINIDUMP_CALLBACK_INPUT, _win32_minidump_callback_input_str, base.minidump_callback_input_str, minidumpapiset/MINIDUMP_CALLBACK_INPUT, minidumpapiset/PMINIDUMP_CALLBACK_INPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_CALLBACK_INPUT
product: Windows
targetos: Windows
req.typenames: MINIDUMP_CALLBACK_INPUT, *PMINIDUMP_CALLBACK_INPUT
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_CALLBACK_INPUT structure


## -description


Contains information used by the 
<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a> function.


## -struct-fields




### -field ProcessId

The identifier of the process that contains callback function.

This member is not used if <b>CallbackType</b> is <b>IoStartCallback</b>.


### -field ProcessHandle

A handle to the process that contains the callback function.

This member is not used if <b>CallbackType</b> is <b>IoStartCallback</b>.


### -field CallbackType

The type of callback function. This member can be one of the values in the 
<a href="https://msdn.microsoft.com/c970564d-e1f0-4317-bf66-752b98767451">MINIDUMP_CALLBACK_TYPE</a> enumeration.


### -field Status

If <b>CallbackType</b> is <b>KernelMinidumpStatusCallback</b>, the union is an <b>HRESULT</b> value that indicates the status of the kernel minidump write attempt.


### -field Thread

If <b>CallbackType</b> is <b>ThreadCallback</b>, the union is a 
<a href="https://msdn.microsoft.com/31da83e6-af8c-440c-b715-78c9c6ac4b9f">MINIDUMP_THREAD_CALLBACK</a> structure.


### -field ThreadEx

If <b>CallbackType</b> is <b>ThreadExCallback</b>, the union is a 
<a href="https://msdn.microsoft.com/a81856df-14a3-42bc-89dc-9796c7b252be">MINIDUMP_THREAD_EX_CALLBACK</a> structure.


### -field Module

If <b>CallbackType</b> is <b>ModuleCallback</b>, the union is a 
<a href="https://msdn.microsoft.com/8ca48df0-ed0e-4ee3-a20a-d89057be37f3">MINIDUMP_MODULE_CALLBACK</a> structure.


### -field IncludeThread

If <b>CallbackType</b> is <b>IncludeThreadCallback</b>, the union is a 
<a href="https://msdn.microsoft.com/4695b739-9af4-4bb8-b7d6-409942bc1932">MINIDUMP_INCLUDE_THREAD_CALLBACK</a> structure.

<b>DbgHelp 6.2 and earlier:  </b>This member is not available.


### -field IncludeModule

If <b>CallbackType</b> is <b>IncludeModuleCallback</b>, the union is a 
<a href="https://msdn.microsoft.com/01dd2217-fd7b-4bcf-a15e-4769c7518741">MINIDUMP_INCLUDE_MODULE_CALLBACK</a> structure.

<b>DbgHelp 6.2 and earlier:  </b>This member is not available.


### -field Io

If <b>CallbackType</b> is <b>IoStartCallback</b>, <b>IoWriteAllCallback</b>, or <b>IoFinishCallback</b>, the union is a <a href="https://msdn.microsoft.com/db38f035-1fb8-4715-846f-59392aac2d4e">MINIDUMP_IO_CALLBACK</a> structure.

<b>DbgHelp 6.4 and earlier:  </b>This member is not available.


### -field ReadMemoryFailure

If <b>CallbackType</b> is <b>ReadMemoryFailureCallback</b>, the union is a <a href="https://msdn.microsoft.com/9710684a-4d08-4ab8-bc33-17c5f01c581f">MINIDUMP_READ_MEMORY_FAILURE_CALLBACK</a> structure.

<b>DbgHelp 6.4 and earlier:  </b>This member is not available.


### -field SecondaryFlags

Contains a value from the <a href="https://msdn.microsoft.com/c8485db1-0cc0-4baa-90fb-b5c1f9236b80">MINIDUMP_SECONDARY_FLAGS</a> enumeration type.

<b>DbgHelp 6.5 and earlier:  </b>This member is not available.


### -field VmQuery

 


### -field VmPreRead

 


### -field VmPostRead

 




## -remarks



If <b>CallbackType</b> is <b>CancelCallback</b> or <b>MemoryCallback</b>, the <b>ProcessId</b>, <b>ProcessHandle</b>, and <b>CallbackType</b> members are valid but no other input is specified.




## -see-also




<a href="https://msdn.microsoft.com/c970564d-e1f0-4317-bf66-752b98767451">MINIDUMP_CALLBACK_TYPE</a>



<a href="https://msdn.microsoft.com/01dd2217-fd7b-4bcf-a15e-4769c7518741">MINIDUMP_INCLUDE_MODULE_CALLBACK</a>



<a href="https://msdn.microsoft.com/4695b739-9af4-4bb8-b7d6-409942bc1932">MINIDUMP_INCLUDE_THREAD_CALLBACK</a>



<a href="https://msdn.microsoft.com/db38f035-1fb8-4715-846f-59392aac2d4e">MINIDUMP_IO_CALLBACK</a>



<a href="https://msdn.microsoft.com/8ca48df0-ed0e-4ee3-a20a-d89057be37f3">MINIDUMP_MODULE_CALLBACK</a>



<a href="https://msdn.microsoft.com/9710684a-4d08-4ab8-bc33-17c5f01c581f">MINIDUMP_READ_MEMORY_FAILURE_CALLBACK</a>



<a href="https://msdn.microsoft.com/31da83e6-af8c-440c-b715-78c9c6ac4b9f">MINIDUMP_THREAD_CALLBACK</a>



<a href="https://msdn.microsoft.com/a81856df-14a3-42bc-89dc-9796c7b252be">MINIDUMP_THREAD_EX_CALLBACK</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

