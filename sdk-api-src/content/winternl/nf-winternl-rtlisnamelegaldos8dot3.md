---
UID: NF:winternl.RtlIsNameLegalDOS8Dot3
title: RtlIsNameLegalDOS8Dot3 function
author: windows-driver-content
description: Determines whether or not a specified name can be used to create a file on the FAT file system.
old-location: winprog\rtlisnamelegaldos8dot3.htm
old-project: DevNotes
ms.assetid: 705fd65a-dd56-46c8-9910-5c07caff9173
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: RtlIsNameLegalDOS8Dot3, RtlIsNameLegalDOS8Dot3 function [Windows API], base.rtlisnamelegaldos8dot3, fs.rtlisnamelegaldos8dot3, winprog.rtlisnamelegaldos8dot3, winternl/RtlIsNameLegalDOS8Dot3
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
-	NtDll.dll
api_name:
-	RtlIsNameLegalDOS8Dot3
product: Windows
targetos: Windows
req.lib: 
req.dll: NtDll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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


### -param OPTIONAL

TBD




#### - NameContainsSpaces [out, optional]

If the function returns <b>TRUE</b>, this parameter indicates whether or not the name 
       contains spaces.

If the function returns <b>FALSE</b>, this parameter is undefined.


#### - OemName [in, out, optional]

A pointer to a buffer that receives the OEM string that corresponds to <i>Name</i>.

This parameter can be <b>NULL</b>.


## -returns



If the specified name forms a valid 8.3 FAT file system name in the current OEM code page, the function 
      returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



This function does not have an associated import library. You must use the 
    <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and 
    <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to
    NtDll.dll.




## -see-also




<a href="https://msdn.microsoft.com/bb0edcc5-4991-47d0-9ade-6c6776a36f39">CheckNameLegalDOS8Dot3</a>
 

 

