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
 

 

