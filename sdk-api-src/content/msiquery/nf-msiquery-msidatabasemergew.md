---
UID: NF:msiquery.MsiDatabaseMergeW
title: MsiDatabaseMergeW function
author: windows-sdk-content
description: The MsiDatabaseMerge function merges two databases together, which allows duplicate rows.
old-location: setup\msidatabasemerge.htm
old-project: Msi
ms.assetid: 2a8c5e13-f7af-47ea-b781-a739d848fe09
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: MsiDatabaseMerge, MsiDatabaseMerge function, MsiDatabaseMergeA, MsiDatabaseMergeW, _msi_msidatabasemerge, msiquery/MsiDatabaseMerge, msiquery/MsiDatabaseMergeA, msiquery/MsiDatabaseMergeW, setup.msidatabasemerge
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
req.unicode-ansi: MsiDatabaseMergeW (Unicode) and MsiDatabaseMergeA (ANSI)
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
api_name:
 - MsiDatabaseMerge
 - MsiDatabaseMergeA
 - MsiDatabaseMergeW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiDatabaseMergeW function


## -description


The 
<b>MsiDatabaseMerge</b> function merges two databases together, which allows duplicate rows. 


## -parameters




### -param hDatabase [in]

The handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>.


### -param hDatabaseMerge [in]

The handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a> to merge into the base database.


### -param szTableName [in]

The name of the table to receive merge conflict information.


## -returns



The 
<b>MsiDatabaseMerge</b> function returns one of the following values:
					

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Row merge conflicts were reported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid or inactive handle was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TABLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid table was supplied.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATATYPE_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Schema difference between the two databases.

</td>
</tr>
</table>
 




## -remarks



The <b>MsiDatabaseMerge</b> function and the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> method of the 
<a href="https://msdn.microsoft.com/97765884-3e1c-486a-932c-6430b113fac8">Database</a> object cannot be used to merge a module that is included in the installation package. They should not be used to merge 
<a href="https://msdn.microsoft.com/673de3ff-e58c-4153-9c8d-c3baebba5eb1">Merge Modules</a> into a Windows Installer package.  To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the <a href="https://msdn.microsoft.com/2c14dfcc-6447-4c08-8e59-f3eaeb621de1">Applying Merge Modules</a> topic.

<b>MsiDatabaseMerge</b> does not copy over embedded 
<a href="https://msdn.microsoft.com/df240302-b875-49bf-8e62-7a35204c35fb">Cabinet Files</a> or 
<a href="https://msdn.microsoft.com/f7b265df-4b34-44ea-85ab-8dbca4797517">embedded transforms</a> from the reference database into the target database. Embedded data streams that are listed in the 
<a href="https://msdn.microsoft.com/44c56407-df2e-4cbe-b7a3-b22e8d97eb03">Binary Table</a> or 
<a href="https://msdn.microsoft.com/a59c552a-21c0-4dd4-9146-88a5f9a22962">Icon Table</a> are copied from the reference database to the target database. Storage embedded in the reference database are not copied to the target database.

The 
<b>MsiDatabaseMerge</b> function merges the data of two databases. These databases must have the same code page. 
<b>MsiDatabaseMerge</b> fails if any tables or rows in the databases conflict. A conflict exists if the data in any row in the first database differs from the data in the corresponding row of the second database. Corresponding rows are in the same table of both databases and have the same primary key in both databases. The tables of non-conflicting databases must have the same number of primary keys, same number of columns, same column types, same column names, and the same data in rows with identical primary keys. Temporary columns however don't matter in the column count and corresponding tables can have a different number of temporary columns without creating conflict as long as the persistent columns match.

If the number, type, or name of columns in corresponding tables are different, the schema of the two databases are incompatible and the installer stops processing tables and the merge fails. The installer checks that the two databases have the same schema before checking for row merge conflicts. If ERROR_DATATYPE_MISMATCH is returned, you are guaranteed that the databases have not been changed.

If the data in particular rows differ, this is a row merge conflict, the installer returns ERROR_FUNCTION_FAILED and creates a new table named <i>szTableName</i>. The first column of this table is the name of the table having the conflict. The second column gives the number of rows in the table having the conflict. The table that reports conflicts appears as follows.

<table>
<tr>
<th>Column</th>
<th>Type</th>
<th>Key</th>
<th>Nullable</th>
</tr>
<tr>
<td>Table</td>
<td>
<a href="https://msdn.microsoft.com/36bedd5d-eb81-4cd5-bd81-634efec8ccf6">Text</a>
</td>
<td>Y</td>
<td>N</td>
</tr>
<tr>
<td>NumRowMergeConflicts</td>
<td>
<a href="https://msdn.microsoft.com/628e385b-8077-4af9-889e-92fa0c172d05">Integer</a>
</td>
<td> </td>
<td>N</td>
</tr>
</table>
 

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/77379664-26f2-4c1d-8c44-d9be2376efa9">Column Definition Format</a>



<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">Database Management Functions</a>
 

 

