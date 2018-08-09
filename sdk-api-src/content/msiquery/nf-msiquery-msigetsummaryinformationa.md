---
UID: NF:msiquery.MsiGetSummaryInformationA
title: MsiGetSummaryInformationA function
author: windows-sdk-content
description: The MsiGetSummaryInformation function obtains a handle to the _SummaryInformation stream for an installer database. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msigetsummaryinformation.htm
old-project: msi
ms.assetid: f3a6d7cc-83b2-45c6-bf86-c579b39c2c92
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MsiGetSummaryInformation, MsiGetSummaryInformation function, MsiGetSummaryInformationA, MsiGetSummaryInformationW, _msi_msigetsummaryinformation, msiquery/MsiGetSummaryInformation, msiquery/MsiGetSummaryInformationA, msiquery/MsiGetSummaryInformationW, setup.msigetsummaryinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetSummaryInformationW (Unicode) and MsiGetSummaryInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InkRecoGuide
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiGetSummaryInformation
 - MsiGetSummaryInformationA
 - MsiGetSummaryInformationW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiGetSummaryInformationA function


## -description


The 
<b>MsiGetSummaryInformation</b> function obtains a handle to the _SummaryInformation stream for an installer database. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters




### -param hDatabase [in]

Handle to the database.


### -param szDatabasePath [in]

Specifies the path to the database.


### -param uiUpdateCount [in]

Specifies the maximum number of updated values.


### -param phSummaryInfo [out]

Pointer to the location from which to receive the summary information handle.


## -returns



The 
<b>MsiGetSummaryInformation</b> function returns the following values:




## -remarks



If the database specified by the 
<b>MsiGetSummaryInformation</b> function is not open, you must specify 0 for <i>hDatabase</i> and specify the path to the database in <i>szDatabasePath</i>. If the database is open, you must set <i>szDatabasePath</i> to 0.

If a value of <i>uiUpdateCount</i> greater than 0 is used to open an existing summary information stream, 
<a href="https://msdn.microsoft.com/76fd8339-2c57-4695-83c7-dcd3cd642f55">MsiSummaryInfoPersist</a> must be called before closing the <i>phSummaryInfo</i> handle. Failing to do this will lose the existing stream information.

To view the summary information of a patch using <b>MsiGetSummaryInformation</b>, set <i>szDatabasePath</i> to the path to the patch. Alternately, you can create a handle to the patch using 
<a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a> and then pass that handle to 
<b>MsiGetSummaryInformation</b> as the <i>hDatabase</i> parameter.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="windows_installer_best_practices.htm">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Summary Information Property Functions</a>



<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>
 

 

