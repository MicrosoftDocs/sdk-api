---
UID: NF:shellapi.SHGetDiskFreeSpaceExA
title: SHGetDiskFreeSpaceExA function
author: windows-sdk-content
description: Retrieves disk space information for a disk volume.
old-location: shell\SHGetDiskFreeSpaceEx.htm
tech.root: shell
ms.assetid: f8adbfa8-124a-4934-b5dc-16e261c15a8b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SHGetDiskFreeSpace, SHGetDiskFreeSpaceEx, SHGetDiskFreeSpaceEx function [Windows Shell], SHGetDiskFreeSpaceExA, SHGetDiskFreeSpaceExW, _shell_SHGetDiskFreeSpaceEx, shell.SHGetDiskFreeSpaceEx, shellapi/SHGetDiskFreeSpaceEx, shellapi/SHGetDiskFreeSpaceExA, shellapi/SHGetDiskFreeSpaceExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetDiskFreeSpaceExW (Unicode) and SHGetDiskFreeSpaceExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetDiskFreeSpaceEx
 - SHGetDiskFreeSpaceExA
 - SHGetDiskFreeSpaceExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetDiskFreeSpaceExA function


## -description


Retrieves disk space information for a disk volume.


## -parameters




### -param pszDirectoryName [in]

Type: <b>LPCTSTR</b>

A null-terminated string that specifies the volume for which size information is retrieved. This can be a drive letter, UNC name, or the path of a folder. You cannot use <b>NULL</b> to represent the current drive.


### -param pulFreeBytesAvailableToCaller [out, optional]

Type: <b><a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>*</b>

Pointer to a value that receives the number of bytes on the volume available to the calling application. If the operating system implements per-user quotas, this value may be less than the total number of free bytes on the volume.


### -param pulTotalNumberOfBytes [out, optional]

Type: <b><a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>*</b>

Pointer to a value that receives the total size of the volume, in bytes.


### -param pulTotalNumberOfFreeBytes [out, optional]

Type: <b><a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>*</b>

Pointer to a value that receives the number of bytes of free space on the volume.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.




## -remarks



The similarly named function <a href="https://msdn.microsoft.com/cfc2be42-3297-4e7c-b082-aa9a40b9821a">SHGetDiskFreeSpace</a> is merely an alias for <b>SHGetDiskFreeSpaceEx</b>. When you call <b>SHGetDiskFreeSpace</b> you actually call this function.

This function calls the <a href="https://msdn.microsoft.com/a52f2dbd-bda6-4217-9e72-f100f8bbe334">GetDiskFreeSpaceEx</a> function if it is available on the operating system. If <b>GetDiskFreeSpaceEx</b> is not available, it is emulated by calling the <a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a> function and manipulating the return values. For additional information, see the documentation for <b>GetDiskFreeSpaceEx</b>.




## -see-also




<a href="https://msdn.microsoft.com/a52f2dbd-bda6-4217-9e72-f100f8bbe334">GetDiskFreeSpaceEx</a>



<a href="https://msdn.microsoft.com/cfc2be42-3297-4e7c-b082-aa9a40b9821a">SHGetDiskFreeSpace</a>
 

 

