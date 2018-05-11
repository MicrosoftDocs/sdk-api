---
UID: NF:winternl.NtOpenFile
title: NtOpenFile function
author: windows-driver-content
description: Opens an existing file, device, directory, or volume, and returns a handle for the file object.
old-location: winprog\ntopenfile.htm
old-project: DevNotes
ms.assetid: b77a85d1-7d2d-4834-b5d9-9baf68804369
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: NtOpenFile, NtOpenFile function [Windows API], winprog.ntopenfile, winternl/NtOpenFile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SYNC_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdll.dll
api_name:
-	NtOpenFile
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
      <b>ZwCreateFile</b> in the WDK.


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
    <a href="https://msdn.microsoft.com/11f09479-e04b-4e5e-bc46-a2d0daf13785">Calling Internal APIs</a>.

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
    <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and 
    <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to 
    Ntdll.dll.



