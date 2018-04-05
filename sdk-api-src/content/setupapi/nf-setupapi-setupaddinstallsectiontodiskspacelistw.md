---
UID: NF:setupapi.SetupAddInstallSectionToDiskSpaceListW
title: SetupAddInstallSectionToDiskSpaceListW function
author: windows-driver-content
description: The SetupAddInstallSectionToDiskSpaceList function searches for CopyFile and DelFile lines in an Install section of an INF file. The function then adds the file operations specified in those sections to a disk-space list.
old-location: setup\setupaddinstallsectiontodiskspacelist.htm
old-project: SetupApi
ms.assetid: 322f36d7-a683-4a48-b294-393277f09e7d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetupAddInstallSectionToDiskSpaceList, SetupAddInstallSectionToDiskSpaceList function [Setup API], SetupAddInstallSectionToDiskSpaceListA, SetupAddInstallSectionToDiskSpaceListW, _setupapi_setupaddinstallsectiontodiskspacelist, setup.setupaddinstallsectiontodiskspacelist, setupapi/SetupAddInstallSectionToDiskSpaceList, setupapi/SetupAddInstallSectionToDiskSpaceListA, setupapi/SetupAddInstallSectionToDiskSpaceListW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupAddInstallSectionToDiskSpaceListW (Unicode) and SetupAddInstallSectionToDiskSpaceListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupAddInstallSectionToDiskSpaceList
-	SetupAddInstallSectionToDiskSpaceListA
-	SetupAddInstallSectionToDiskSpaceListW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
 

 

