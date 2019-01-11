---
UID: NF:winternl.NtQueryMultipleValueKey
title: NtQueryMultipleValueKey function
author: windows-sdk-content
description: Retrieves values for the specified multiple-value key.
old-location: winprog\ntquerymultiplevaluekey.htm
tech.root: DevNotes
ms.assetid: fe78446c-b936-4ded-846a-f3ca26eff06e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NtQueryMultipleValueKey, NtQueryMultipleValueKey function [Windows API], base.ntquerymultiplevaluekey, winprog.ntquerymultiplevaluekey, winternl/NtQueryMultipleValueKey
ms.topic: function
req.header: winternl.h
req.include-header: 
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
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - NtQueryMultipleValueKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NtQueryMultipleValueKey function


## -description


<p class="CCE_Message">[This function may be changed or removed from Windows without further notice.]

Retrieves values for the specified multiple-value key.


## -parameters




### -param KeyHandle [in]

A handle to the key for which to retrieve values. The handle must be opened with the <b>KEY_QUERY_VALUE</b> access right.


### -param ValueEntries [in, out]

A pointer to an array of <a href="http://go.microsoft.com/fwlink/p/?linkid=119324">KEY_VALUE_ENTRY</a> structures containing the names of values to retrieve.


### -param EntryCount [in]

The number of elements in the <i>ValueEntries</i> array.


### -param ValueBuffer [out]

A pointer to a buffer to receive the values. 


### -param BufferLength [in, out]

A pointer to a variable that contains the size of the buffer at <i>ValueBuffer</i>, in bytes. When the function returns, the <i>BufferLength</i> parameter contains the number of bytes written to the buffer at <i>ValueBuffer</i>. 


### -param RequiredBufferLength [out, optional]

A pointer to a variable to receive the number of bytes required for all of the values to be returned by the function. This parameter can be <b>NULL</b>.


## -returns



Returns an <b>NTSTATUS</b> or error code.

If the buffer is too small to hold the information to be retrieved, the function returns <b>STATUS_BUFFER_OVERFLOW</b> and, if the <i>RequiredBufferLength</i> parameter is specified, sets it to the buffer size required.

The forms and significance of <b>NTSTATUS</b> error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.




## -remarks



This function has no associated header file. The associated import library, Ntdll.lib, is available in the WDK. You can also use the <a href="https://msdn.microsoft.com/191fcbd8-4542-4cad-955e-6951f3005fc5">LoadLibrary</a> and <a href="https://msdn.microsoft.com/e425948c-5588-4a4f-994c-4e608af18439">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>
 

 

