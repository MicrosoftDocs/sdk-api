---
UID: NF:msiquery.MsiDatabaseMergeA
title: MsiDatabaseMergeA function (msiquery.h)
description: The MsiDatabaseMerge function merges two databases together, which allows duplicate rows. (ANSI)
helpviewer_keywords: ["MsiDatabaseMergeA", "msiquery/MsiDatabaseMergeA"]
old-location: setup\msidatabasemerge.htm
tech.root: setup
ms.assetid: 2a8c5e13-f7af-47ea-b781-a739d848fe09
ms.date: 12/05/2018
ms.keywords: MsiDatabaseMerge, MsiDatabaseMerge function, MsiDatabaseMergeA, MsiDatabaseMergeW, _msi_msidatabasemerge, msiquery/MsiDatabaseMerge, msiquery/MsiDatabaseMergeA, msiquery/MsiDatabaseMergeW, setup.msidatabasemerge
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiDatabaseMergeA
 - msiquery/MsiDatabaseMergeA
dev_langs:
 - c++
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
---

# MsiDatabaseMergeA function


## -description

The 
<b>MsiDatabaseMerge</b> function merges two databases together, which allows duplicate rows.

## -parameters

### -param hDatabase [in]

The handle to the database obtained from <a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a>.

### -param hDatabaseMerge [in]

The handle to the database obtained from <a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a> to merge into the base database.

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

The <b>MsiDatabaseMerge</b> function and the <a href="/windows/desktop/Msi/database-merge">Merge</a> method of the 
<a href="/windows/desktop/Msi/database-object">Database</a> object cannot be used to merge a module that is included in the installation package. They should not be used to merge 
<a href="/windows/desktop/Msi/merge-modules">Merge Modules</a> into a Windows Installer package.  To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the <a href="/windows/desktop/Msi/applying-merge-modules">Applying Merge Modules</a> topic.

<b>MsiDatabaseMerge</b> does not copy over embedded 
<a href="/windows/desktop/Msi/cabinet-files">Cabinet Files</a> or 
<a href="/windows/desktop/Msi/embedded-transforms">embedded transforms</a> from the reference database into the target database. Embedded data streams that are listed in the 
<a href="/windows/desktop/Msi/binary-table">Binary Table</a> or 
<a href="/windows/desktop/Msi/icon-table">Icon Table</a> are copied from the reference database to the target database. Storage embedded in the reference database are not copied to the target database.

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
<a href="/windows/desktop/Msi/text">Text</a>
</td>
<td>Y</td>
<td>N</td>
</tr>
<tr>
<td>NumRowMergeConflicts</td>
<td>
<a href="/windows/desktop/Msi/integer">Integer</a>
</td>
<td> </td>
<td>N</td>
</tr>
</table>
 

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiDatabaseMerge as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/column-definition-format">Column Definition Format</a>



<a href="/windows/desktop/Msi/database-functions">Database Management Functions</a>
