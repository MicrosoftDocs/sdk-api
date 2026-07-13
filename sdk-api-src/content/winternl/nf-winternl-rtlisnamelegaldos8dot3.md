---
UID: NF:winternl.RtlIsNameLegalDOS8Dot3
title: RtlIsNameLegalDOS8Dot3 function (winternl.h)
description: Determines whether or not a specified name can be used to create a file on the FAT file system.
helpviewer_keywords: ["RtlIsNameLegalDOS8Dot3","RtlIsNameLegalDOS8Dot3 function [Windows API]","base.rtlisnamelegaldos8dot3","fs.rtlisnamelegaldos8dot3","winprog.rtlisnamelegaldos8dot3","winternl/RtlIsNameLegalDOS8Dot3"]
old-location: winprog\rtlisnamelegaldos8dot3.htm
tech.root: winprog
ms.assetid: 705fd65a-dd56-46c8-9910-5c07caff9173
ms.date: 12/05/2018
ms.keywords: RtlIsNameLegalDOS8Dot3, RtlIsNameLegalDOS8Dot3 function [Windows API], base.rtlisnamelegaldos8dot3, fs.rtlisnamelegaldos8dot3, winprog.rtlisnamelegaldos8dot3, winternl/RtlIsNameLegalDOS8Dot3
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlIsNameLegalDOS8Dot3
 - winternl/RtlIsNameLegalDOS8Dot3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtDll.dll
api_name:
 - RtlIsNameLegalDOS8Dot3
---

# RtlIsNameLegalDOS8Dot3 function


## -description

<p class="CCE_Message">[<b>RtlIsNameLegalDOS8Dot3</b> 
    is available for use in Windows XP. It may be altered or unavailable in 
    subsequent versions. Applications that target a minimum of Windows Server 2003 and 
    Windows XP with Service Pack 1 (SP1) and later should use the <b>CheckNameLegalDOS8Dot3</b> 
    function.]

Determines whether or not a specified name can be used to create a file on the FAT file 
   system.

## -parameters

### -param Name [in]

The file name, in 8.3 format.

### -param OemName [in, out, optional]

A pointer to a buffer that receives the OEM string that corresponds to <i>Name</i>.

This parameter can be <b>NULL</b>.

### -param NameContainsSpaces [out, optional]

If the function returns <b>TRUE</b>, this parameter indicates whether or not the name 
       contains spaces.

If the function returns <b>FALSE</b>, this parameter is undefined.

## -returns

If the specified name forms a valid 8.3 FAT file system name in the current OEM code page, the function 
      returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

## -remarks

This function does not have an associated import library. You must use the 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to
    NtDll.dll.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-checknamelegaldos8dot3a">CheckNameLegalDOS8Dot3</a>