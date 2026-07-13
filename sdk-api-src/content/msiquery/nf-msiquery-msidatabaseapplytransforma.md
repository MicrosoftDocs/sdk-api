---
UID: NF:msiquery.MsiDatabaseApplyTransformA
title: MsiDatabaseApplyTransformA function (msiquery.h)
description: The MsiDatabaseApplyTransform function applies a transform to a database. (ANSI)
helpviewer_keywords: ["MSITRANSFORM_ERROR_ADDEXISTINGROW", "MSITRANSFORM_ERROR_ADDEXISTINGTABLE", "MSITRANSFORM_ERROR_CHANGECODEPAGE", "MSITRANSFORM_ERROR_DELMISSINGROW", "MSITRANSFORM_ERROR_DELMISSINGTABLE", "MSITRANSFORM_ERROR_UPDATEMISSINGROW", "MSITRANSFORM_ERROR_VIEWTRANSFORM", "MsiDatabaseApplyTransformA", "msiquery/MsiDatabaseApplyTransformA"]
old-location: setup\msidatabaseapplytransform.htm
tech.root: setup
ms.assetid: a0222465-f778-43c1-8007-22df6a01f8bd
ms.date: 12/05/2018
ms.keywords: MSITRANSFORM_ERROR_ADDEXISTINGROW, MSITRANSFORM_ERROR_ADDEXISTINGTABLE, MSITRANSFORM_ERROR_CHANGECODEPAGE, MSITRANSFORM_ERROR_DELMISSINGROW, MSITRANSFORM_ERROR_DELMISSINGTABLE, MSITRANSFORM_ERROR_UPDATEMISSINGROW, MSITRANSFORM_ERROR_VIEWTRANSFORM, MsiDatabaseApplyTransform, MsiDatabaseApplyTransform function, MsiDatabaseApplyTransformA, MsiDatabaseApplyTransformW, _msi_msidatabaseapplytransform, msiquery/MsiDatabaseApplyTransform, msiquery/MsiDatabaseApplyTransformA, msiquery/MsiDatabaseApplyTransformW, setup.msidatabaseapplytransform
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDatabaseApplyTransformW (Unicode) and MsiDatabaseApplyTransformA (ANSI)
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
 - MsiDatabaseApplyTransformA
 - msiquery/MsiDatabaseApplyTransformA
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
 - MsiDatabaseApplyTransform
 - MsiDatabaseApplyTransformA
 - MsiDatabaseApplyTransformW
---

# MsiDatabaseApplyTransformA function


## -description

The 
<b>MsiDatabaseApplyTransform</b> function applies a transform to a database.

## -parameters

### -param hDatabase [in]

Handle to the database obtained from <a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a> to the transform.

### -param szTransformFile [in]

Specifies the name of the transform file to apply.

### -param iErrorConditions [in]

Error conditions that should be suppressed. This parameter is a bit field that can contain the following bits. 



<table>
<tr>
<th>Error condition</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_ADDEXISTINGROW"></a><a id="msitransform_error_addexistingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_ADDEXISTINGROW</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Adding a row that already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_DELMISSINGROW"></a><a id="msitransform_error_delmissingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_DELMISSINGROW</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Deleting a row that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_ADDEXISTINGTABLE"></a><a id="msitransform_error_addexistingtable"></a><dl>
<dt><b>MSITRANSFORM_ERROR_ADDEXISTINGTABLE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Adding a table that already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_DELMISSINGTABLE"></a><a id="msitransform_error_delmissingtable"></a><dl>
<dt><b>MSITRANSFORM_ERROR_DELMISSINGTABLE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Deleting a table that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_UPDATEMISSINGROW"></a><a id="msitransform_error_updatemissingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_UPDATEMISSINGROW</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Updating a row that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_CHANGECODEPAGE"></a><a id="msitransform_error_changecodepage"></a><dl>
<dt><b>MSITRANSFORM_ERROR_CHANGECODEPAGE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Transform and database code pages do not match and neither has a neutral code page.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_VIEWTRANSFORM"></a><a id="msitransform_error_viewtransform"></a><dl>
<dt><b>MSITRANSFORM_ERROR_VIEWTRANSFORM</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Create the temporary 
<a href="/windows/desktop/Msi/-transformview-table">_TransformView table</a>.

</td>
</tr>
</table>

## -returns

The 
<b>MsiDatabaseApplyTransform</b> function returns one of the following values:

## -remarks

The 
<b>MsiDatabaseApplyTransform</b> function delays transforming tables until it is necessary. Any tables to be added or dropped are processed immediately. However, changes to the existing table are delayed until the table is loaded or the database is committed.

An error occurs if 
<b>MsiDatabaseApplyTransform</b> is called when tables have already been loaded and saved to storage.

Because the list delimiter for transforms, sources and patches is a semicolon, this character should not be used for filenames or paths.

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiDatabaseApplyTransform as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Database Management Functions</a>



<a href="/windows/desktop/Msi/database-transforms">Database Transforms</a>
