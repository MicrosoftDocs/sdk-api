---
UID: NF:ntmsapi.ExportNtmsDatabase
title: ExportNtmsDatabase function (ntmsapi.h)
author: windows-sdk-content
description: The ExportNtmsDatabase function creates a consistent set of database files in the RSM database directory.
old-location: fs\exportntmsdatabase.htm
tech.root: Rsm
ms.assetid: 0c6df5d3-c771-4749-8fbd-de5c02ffa5d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExportNtmsDatabase, ExportNtmsDatabase function [Files], _zaw_exportntmsdatabase, base.exportntmsdatabase, fs.exportntmsdatabase, ntmsapi/ExportNtmsDatabase
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - ExportNtmsDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ExportNtmsDatabase function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ExportNtmsDatabase</b> function creates a consistent set of database files in the RSM database directory.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access to one or more RSM objects is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database query or update failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHARING_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
One of the files that the function must write to is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



The 
<b>ExportNtmsDatabase</b> function is used by backup applications to create a copy of the RSM database. Any existing files in the Export directory are overwritten by this function.

The default location of the database is%SystemRoot%\System32\NtmsData, but this can be set by defining a registry value:

<b>HKLM</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Control</b>\<b>NTMS</b>\<b>NtmsData</b>

This function creates a subdirectory called Export and places the consistent files there.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Database Backup and Recovery Functions</a>



<a href="https://msdn.microsoft.com/9bb41109-6548-4d22-92c8-0d8ed960f119">ImportNtmsDatabase</a>
 

 

