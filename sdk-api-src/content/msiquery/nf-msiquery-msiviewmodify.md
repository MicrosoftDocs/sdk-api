---
UID: NF:msiquery.MsiViewModify
title: MsiViewModify function (msiquery.h)
description: The MsiViewModify function updates a fetched record.
helpviewer_keywords: ["MSIMODIFY_ASSIGN","MSIMODIFY_DELETE","MSIMODIFY_INSERT","MSIMODIFY_INSERT_TEMPORARY","MSIMODIFY_MERGE","MSIMODIFY_REFRESH","MSIMODIFY_REPLACE","MSIMODIFY_SEEK","MSIMODIFY_UPDATE","MSIMODIFY_VALIDATE","MSIMODIFY_VALIDATE_DELETE","MSIMODIFY_VALIDATE_FIELD","MSIMODIFY_VALIDATE_NEW","MsiViewModify","MsiViewModify function","_msi_msiviewmodify","msiquery/MsiViewModify","setup.msiviewmodify"]
old-location: setup\msiviewmodify.htm
tech.root: setup
ms.assetid: 312c3e62-4c08-447b-951f-d8d944daff3e
ms.date: 12/05/2018
ms.keywords: MSIMODIFY_ASSIGN, MSIMODIFY_DELETE, MSIMODIFY_INSERT, MSIMODIFY_INSERT_TEMPORARY, MSIMODIFY_MERGE, MSIMODIFY_REFRESH, MSIMODIFY_REPLACE, MSIMODIFY_SEEK, MSIMODIFY_UPDATE, MSIMODIFY_VALIDATE, MSIMODIFY_VALIDATE_DELETE, MSIMODIFY_VALIDATE_FIELD, MSIMODIFY_VALIDATE_NEW, MsiViewModify, MsiViewModify function, _msi_msiviewmodify, msiquery/MsiViewModify, setup.msiviewmodify
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiViewModify
 - msiquery/MsiViewModify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiViewModify
---

# MsiViewModify function


## -description

The 
<b>MsiViewModify</b> function updates a fetched record.

## -parameters

### -param hView [in]

Handle to a view.

### -param eModifyMode [in]

Specifies the modify mode. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_SEEK"></a><a id="msimodify_seek"></a><dl>
<dt><b>MSIMODIFY_SEEK</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Refreshes the information in the supplied record without changing the position in the result set and without affecting subsequent fetch operations. The record may then be used for subsequent Update, Delete, and Refresh. All primary key columns of the table must be in the query and the record must have at least as many fields as the query. Seek cannot be used with multi-table queries. This mode cannot be used with a view containing joins. See also the remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_REFRESH"></a><a id="msimodify_refresh"></a><dl>
<dt><b>MSIMODIFY_REFRESH</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Refreshes the information in the record. Must first call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a> with the same record. Fails for a deleted row. Works with read-write and read-only records.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_INSERT"></a><a id="msimodify_insert"></a><dl>
<dt><b>MSIMODIFY_INSERT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Inserts a record. Fails if a row with the same primary keys exists. Fails with a read-only database. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_UPDATE"></a><a id="msimodify_update"></a><dl>
<dt><b>MSIMODIFY_UPDATE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Updates an existing record. Nonprimary keys only. Must first call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a>. Fails with a deleted record. Works only with read-write records.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_ASSIGN"></a><a id="msimodify_assign"></a><dl>
<dt><b>MSIMODIFY_ASSIGN</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Writes current data in the cursor to a table row. Updates record if the primary keys match an existing row and inserts if they do not match. Fails with a read-only database. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_REPLACE"></a><a id="msimodify_replace"></a><dl>
<dt><b>MSIMODIFY_REPLACE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Updates or deletes and inserts a record into a table. Must first call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a> with the same record. Updates record if the primary keys are unchanged. Deletes old row and inserts new if primary keys have changed. Fails with a read-only database. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_MERGE"></a><a id="msimodify_merge"></a><dl>
<dt><b>MSIMODIFY_MERGE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Inserts or validates a record in a table. Inserts if primary keys do not match any row and validates if there is a match. Fails if the record does not match the data in the table. Fails if there is a record with a duplicate key that is not identical. Works only with read-write records. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_DELETE"></a><a id="msimodify_delete"></a><dl>
<dt><b>MSIMODIFY_DELETE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Remove a row from the table. You must first call the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a> function with the same record. Fails if the row has been deleted. Works only with read-write records. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_INSERT_TEMPORARY"></a><a id="msimodify_insert_temporary"></a><dl>
<dt><b>MSIMODIFY_INSERT_TEMPORARY</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Inserts a temporary record. The information is not persistent. Fails if a row with the same primary key exists. Works only with read-write records. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_VALIDATE"></a><a id="msimodify_validate"></a><dl>
<dt><b>MSIMODIFY_VALIDATE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Validates a record. Does not validate across joins. You must first call the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a> function with the same record. Obtain validation errors with 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewgeterrora">MsiViewGetError</a>. Works with read-write and read-only records. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_VALIDATE_NEW"></a><a id="msimodify_validate_new"></a><dl>
<dt><b>MSIMODIFY_VALIDATE_NEW</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Validate a new record. Does not validate across joins. Checks for duplicate keys. Obtain validation errors by calling 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewgeterrora">MsiViewGetError</a>. Works with read-write and read-only records. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_VALIDATE_FIELD"></a><a id="msimodify_validate_field"></a><dl>
<dt><b>MSIMODIFY_VALIDATE_FIELD</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Validates fields of a fetched or new record. Can validate one or more fields of an incomplete record. Obtain validation errors by calling 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewgeterrora">MsiViewGetError</a>. Works with read-write and read-only records. This mode cannot be used with a view containing joins.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIMODIFY_VALIDATE_DELETE"></a><a id="msimodify_validate_delete"></a><dl>
<dt><b>MSIMODIFY_VALIDATE_DELETE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Validates a record that will be deleted later. You must first call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a>. Fails if another row refers to the primary keys of this row. Validation does not check for the existence of the primary keys of this row in properties or strings. Does not check if a column is a foreign key to multiple tables. Obtain validation errors by calling 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewgeterrora">MsiViewGetError</a>. Works with read-write and read-only records. This mode cannot be used with a view that contains joins.

</td>
</tr>
</table>

### -param hRecord [in]

Handle to the record to modify.

## -returns

The 
<b>MsiViewModify</b> function returns the following values:

Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.

## -remarks

The MSIMODIFY_VALIDATE, MSIMODIFY_VALIDATE_NEW, MSIMODIFY_VALIDATE_FIELD, and MSIMODIFY_VALIDATE_DELETE values of the 
<b>MsiViewModify</b> function do not perform actual updates; they ensure that the data in the record is valid. Use of these validation enumerations requires that the database contains the 
<a href="/windows/desktop/Msi/-validation-table">_Validation table</a>.

You can call MSIMODIFY_UPDATE or MSIMODIFY_DELETE with a record immediately after using MSIMODIFY_INSERT, MSIMODIFY_INSERT_TEMPORARY, or MSIMODIFY_SEEK provided you have NOT modified the 0th field of the inserted or sought record.

To execute any SQL statement, a view must be created. However, a view that does not create a result set, such as CREATE TABLE, or INSERT INTO, cannot be used with 
<b>MsiViewModify</b> to update tables though the view.

You cannot fetch a record that contains binary data from one database and then use that record to insert the data into another database. To move binary data from one database to another, you should export the data to a file and then import it into the new database using a query and the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msirecordsetstreama">MsiRecordSetStream</a>. This ensures that each database has its own copy of the binary data.

Note that custom actions can only add, modify, or remove temporary rows, columns, or tables from a database. Custom actions cannot modify persistent data in a database, such as data that is a part of the database stored on disk. For more information, see 
<a href="/windows/desktop/Msi/accessing-the-current-installer-session-from-inside-a-custom-action">Accessing the Current Installer Session from Inside a Custom Action</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>