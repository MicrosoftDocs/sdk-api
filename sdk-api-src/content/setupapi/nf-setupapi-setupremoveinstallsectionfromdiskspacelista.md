---
UID: NF:setupapi.SetupRemoveInstallSectionFromDiskSpaceListA
title: SetupRemoveInstallSectionFromDiskSpaceListA function
author: windows-sdk-content
description: The SetupRemoveInstallSectionFromDiskSpaceList function searches an Install section of an INF file for CopyFiles and DelFiles lines, and removes the file operations specified in those sections from a disk-space list.
old-location: setup\setupremoveinstallsectionfromdiskspacelist.htm
old-project: SetupApi
ms.assetid: dd104c59-faee-4eb6-abbc-a4c13d766298
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SetupRemoveInstallSectionFromDiskSpaceList, SetupRemoveInstallSectionFromDiskSpaceList function [Setup API], SetupRemoveInstallSectionFromDiskSpaceListA, SetupRemoveInstallSectionFromDiskSpaceListW, _setupapi_setupremoveinstallsectionfromdiskspacelist, setup.setupremoveinstallsectionfromdiskspacelist, setupapi/SetupRemoveInstallSectionFromDiskSpaceList, setupapi/SetupRemoveInstallSectionFromDiskSpaceListA, setupapi/SetupRemoveInstallSectionFromDiskSpaceListW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRemoveInstallSectionFromDiskSpaceListW (Unicode) and SetupRemoveInstallSectionFromDiskSpaceListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupRemoveInstallSectionFromDiskSpaceList
 - SetupRemoveInstallSectionFromDiskSpaceListA
 - SetupRemoveInstallSectionFromDiskSpaceListW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupRemoveInstallSectionFromDiskSpaceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupRemoveInstallSectionFromDiskSpaceList</b> function searches an <b>Install</b> section of an INF file for <b>CopyFiles</b> and <b>DelFiles</b> lines, and removes the file operations specified in those sections from a disk-space list.


## -parameters




### -param DiskSpace [in]

Handle to a disk-space list.


### -param InfHandle [in]

Handle to an open INF file that contains the <b>Install</b> section. If <i>LayoutInfHandle</i> is not specified, the INF file must also contain the section specified by <i>SectionName</i>. 


### -param LayoutInfHandle [in]

Optional handle to the INF file that contains the <b>SourceDisksFiles</b> sections. Otherwise, that section is assumed to exist in the INF file specified by <i>InfHandle</i>.


### -param SectionName [in]

Pointer to a null-terminated string that specifies the name of the section to be added to the disk-space list.


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



<a href="https://msdn.microsoft.com/322f36d7-a683-4a48-b294-393277f09e7d">SetupAddInstallSectionToDiskSpaceList</a>



<a href="https://msdn.microsoft.com/0d23c8ce-ada6-4640-b9ad-8989f9a122a2">SetupRemoveFromDiskSpaceList</a>



<a href="https://msdn.microsoft.com/0ac9becd-bdd5-4017-b880-4f226150d275">SetupRemoveSectionFromDiskSpaceList</a>
 

 

