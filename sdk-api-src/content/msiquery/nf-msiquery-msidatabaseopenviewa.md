---
UID: NF:msiquery.MsiDatabaseOpenViewA
title: MsiDatabaseOpenViewA function
author: windows-sdk-content
description: The MsiDatabaseOpenView function prepares a database query and creates a view object. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msidatabaseopenview.htm
old-project: Msi
ms.assetid: 1ef23f9a-7d79-4d07-9349-8e9c132f1b94
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: MsiDatabaseOpenView, MsiDatabaseOpenView function, MsiDatabaseOpenViewA, MsiDatabaseOpenViewW, _msi_msidatabaseopenview, msiquery/MsiDatabaseOpenView, msiquery/MsiDatabaseOpenViewA, msiquery/MsiDatabaseOpenViewW, setup.msidatabaseopenview
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
req.unicode-ansi: MsiDatabaseOpenViewW (Unicode) and MsiDatabaseOpenViewA (ANSI)
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
 - MsiDatabaseOpenView
 - MsiDatabaseOpenViewA
 - MsiDatabaseOpenViewW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiDatabaseOpenViewA function


## -description


The 
<b>MsiDatabaseOpenView</b> function prepares a database query and creates a view object. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters




### -param hDatabase [in]

Handle to the database to which you want to open a view object. You can get the handle as described in <a href="https://msdn.microsoft.com/53cf73bc-4d52-471c-8384-46d106a36e38">Obtaining a Database Handle</a>.


### -param szQuery [in]

Specifies a SQL query string for querying the database. For correct syntax, see 
<a href="https://msdn.microsoft.com/badee528-fa69-43ab-965e-d9e6f2529b99">SQL Syntax</a>.


### -param phView [out]

Pointer to a handle for the returned view.


## -returns



The 
<b>MsiDatabaseOpenView</b> function  returns one of the following values:
					




## -remarks



The 
<b>MsiDatabaseOpenView</b> function opens a view object for a database. You must open a view object for a database before performing any execution or fetching.

If an error occurs, you can call 
<a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a> for more information.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="https://msdn.microsoft.com/library/Bb204770(v=VS.85).aspx">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">General Database Access Functions</a>
 

 

