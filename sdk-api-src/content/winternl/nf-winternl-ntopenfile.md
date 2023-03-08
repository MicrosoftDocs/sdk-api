---
UID: NF:winternl.NtOpenFile
title: NtOpenFile function (winternl.h)
description: Opens an existing file, device, directory, or volume, and returns a handle for the file object.
helpviewer_keywords: ["NtOpenFile","NtOpenFile function [Windows API]","winprog.ntopenfile","winternl/NtOpenFile"]
old-location: winprog\ntopenfile.htm
tech.root: winprog
ms.assetid: b77a85d1-7d2d-4834-b5d9-9baf68804369
ms.date: 12/05/2018
ms.keywords: NtOpenFile, NtOpenFile function [Windows API], winprog.ntopenfile, winternl/NtOpenFile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtOpenFile
 - winternl/NtOpenFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtOpenFile
---

# NtOpenFile function


## -description

Opens an existing file, device, directory, or volume, and returns a handle for the file 
    object.

This function is equivalent to the <b>ZwOpenFile</b> function documented in the 
    Windows Driver Kit (WDK).

## -parameters

### -param FileHandle [out]

A pointer to a handle for the opened file. The driver must close the handle with 
      <b>ZwClose</b> once the handle is no longer in use.

### -param DesiredAccess [in]

The <b>ACCESS_MASK</b> value that expresses the types of file access desired by the 
      caller. For information about the types of access that can be specified, see 
      <b>ZwCreateFile</b> in the WDK.

### -param ObjectAttributes [in]

A pointer to a structure that a caller initializes with 
      <b>InitializeObjectAttributes</b>. If the caller is not running in the system process 
      context, it must set the <b>OBJ_KERNEL_HANDLE</b> attribute for 
      <i>ObjectAttributes</i>. For more information about specifying object attributes, see 
      the <i>CreateOptions</i> parameter of <b>ZwCreateFile</b> in the WDK.

### -param IoStatusBlock [out]

A pointer to a structure that contains information about the requested operation and the final completion 
      status.

### -param ShareAccess [in]

The type of share access for the file. For more information, see 
      <b>ZwCreateFile</b> in the WDK.

### -param OpenOptions [in]

The options to be applied when opening the file. For more information, see 
       <b>ZwCreateFile</b> in the WDK.

## -returns

<b>NtOpenFile</b> either returns 
       <b>STATUS_SUCCESS</b> or an appropriate error status. If it returns an error status, the 
       caller can find additional information about the cause of the failure by checking the 
       <i>IoStatusBlock</i>.

## -remarks

Before using this function, please read 
    <a href="/windows/desktop/DevNotes/calling-internal-apis">Calling Internal APIs</a>.

Driver routines that run in a process context other than that of the system process must set the 
     <b>OBJ_KERNEL_HANDLE</b> attribute for the <i>ObjectAttributes</i> 
     parameter of <b>ZwOpenFile</b>. This restricts the use of the handle returned by 
     <b>ZwOpenFile</b> to processes running only in kernel mode. Otherwise, the handle can 
     be accessed by the process in whose context the driver is running. Drivers can call 
     <b>InitializeObjectAttributes</b> to set the 
     <b>OBJ_KERNEL_HANDLE</b> attribute as follows.

<code>InitializeObjectAttributes(&amp;ObjectAddributes, NULL, OBJ_KERNEL_HANDLE, NULL, NULL);</code>

Callers of <b>ZwCreateFile</b> must be running at IRQL = PASSIVE_LEVEL.

Note that the WDK header file Ntdef.h is necessary for many constant definitions 
    as well as the <b>InitializeObjectAttributes</b> macro. The associated import library, 
    Ntdll.lib is available in the WDK. You can also use the 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to 
    Ntdll.dll.
