---
UID: NF:msi.MsiCloseHandle
title: MsiCloseHandle function
author: windows-sdk-content
description: The MsiCloseHandle function closes an open installation handle.
old-location: setup\msiclosehandle.htm
old-project: Msi
ms.assetid: b9e90ed4-fda8-4628-a713-67c651e1b572
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiCloseHandle, MsiCloseHandle function, _msi_msiclosehandle, msi/MsiCloseHandle, setup.msiclosehandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
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
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
-	Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
-	MsiCloseHandle
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiCloseHandle function


## -description


The 
<b>MsiCloseHandle</b> function closes an open installation handle.


## -parameters




### -param hAny [in]

Specifies any open installation handle.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid handle was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



<b>MsiCloseHandle</b> must be called from the same thread that requested the creation of the handle.

The following functions supply handles that should be closed after use by calling 
<b>MsiCloseHandle</b>:

<a href="https://msdn.microsoft.com/fc1d5a09-3097-4a1c-a615-1b93f7eacb04">MsiCreateRecord</a>
<a href="https://msdn.microsoft.com/148d467f-fecd-42a9-b838-22799a159f97">MsiGetActiveDatabase</a>
<a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>
<a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>
<a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>
<a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>
<a href="https://msdn.microsoft.com/1ef23f9a-7d79-4d07-9349-8e9c132f1b94">MsiDatabaseOpenView</a>
<a href="https://msdn.microsoft.com/1a973a22-ca3a-4980-9b20-d3c5b43fdd19">MsiViewFetch</a>
<a href="https://msdn.microsoft.com/f1b8e24c-ac90-4a25-a1d1-c005c403dffc">MsiViewGetColumnInfo</a>
<a href="https://msdn.microsoft.com/08ceaf05-a64b-41ac-964b-ae4648e42bae">MsiDatabaseGetPrimaryKeys</a>
<a href="https://msdn.microsoft.com/f3a6d7cc-83b2-45c6-bf86-c579b39c2c92">MsiGetSummaryInformation</a>
<a href="https://msdn.microsoft.com/77df6829-119d-4fe6-96b0-c75381b9de6c">MsiEnableUIPreview</a>
Note that when writing custom actions, it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<b>MsiCloseHandle</b>.

For example, if you use code like this:

MSIHANDLE hRec = MsiCreateRecord(3);

Change it to:

PMSIHANDLE hRec = MsiCreateRecord(3);




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Handle Management Functions</a>
 

 

