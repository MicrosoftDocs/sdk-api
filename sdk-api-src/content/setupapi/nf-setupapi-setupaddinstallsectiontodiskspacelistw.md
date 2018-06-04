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

# SetupAddInstallSectionToDiskSpaceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupAddInstallSectionToDiskSpaceList</b> function searches for <b>CopyFile</b> and <b>DelFile</b> lines in an <b>Install</b> section of an INF file. The function then adds the file operations specified in those sections to a disk-space list.


## -parameters




### -param DiskSpace [in]

Handle to a disk-space list.


### -param InfHandle [in]

Handle to an open INF file that contains the <b>Install</b> section to be searched. If <i>ListInfHandle</i> is not specified, the INF file must also contain the section specified by <i>SectionName</i>. 


### -param LayoutInfHandle [in]

This parameter, if specified, provides the handle to the INF file that contains the <b>SourceDisksFiles</b> sections. Otherwise that section is assumed to exist in the INF file specified by <i>InfHandle</i>.


### -param SectionName [in]

Name of the Install section to be added to the disk-space list. You should use a null-terminated string.


### -param Reserved1 [in]

Must be zero.


### -param Reserved2 [in]

Must be zero.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function requires a Windows INF file. Some older INF file  formats may not be supported. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/8225d0b4-b750-4580-83f5-dcffdf2ee67b">SetupAddSectionToDiskSpaceList</a>



<a href="https://msdn.microsoft.com/f1bb7096-b4a6-450b-9552-9a3dc4c71f24">SetupAddToDiskSpaceList</a>



<a href="https://msdn.microsoft.com/dd104c59-faee-4eb6-abbc-a4c13d766298">SetupRemoveInstallSectionFromDiskSpaceList</a>
 

 

