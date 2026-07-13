---
UID: NF:msiquery.MsiCreateTransformSummaryInfoA
title: MsiCreateTransformSummaryInfoA function (msiquery.h)
description: The MsiCreateTransformSummaryInfo function creates summary information of an existing transform to include validation and error conditions. Execution of this function sets the error record, which is accessible by using MsiGetLastErrorRecord. (ANSI)
helpviewer_keywords: ["MSITRANSFORM_ERROR_ADDEXISTINGROW", "MSITRANSFORM_ERROR_ADDEXISTINGTABLE", "MSITRANSFORM_ERROR_CHANGECODEPAGE", "MSITRANSFORM_ERROR_DELMISSINGROW", "MSITRANSFORM_ERROR_DELMISSINGTABLE", "MSITRANSFORM_ERROR_UPDATEMISSINGROW", "MSITRANSFORM_VALIDATE_LANGUAGE", "MSITRANSFORM_VALIDATE_MAJORVERSION", "MSITRANSFORM_VALIDATE_MINORVERSION", "MSITRANSFORM_VALIDATE_NEWEQUALBASEVERSION", "MSITRANSFORM_VALIDATE_NEWGREATERBASEVERSION", "MSITRANSFORM_VALIDATE_NEWGREATEREQUALBASEVERSION", "MSITRANSFORM_VALIDATE_NEWLESSBASEVERSION", "MSITRANSFORM_VALIDATE_NEWLESSEQUALBASEVERSION", "MSITRANSFORM_VALIDATE_PRODUCT", "MSITRANSFORM_VALIDATE_UPDATEVERSION", "MSITRANSFORM_VALIDATE_UPGRADECODE", "MsiCreateTransformSummaryInfoA", "msiquery/MsiCreateTransformSummaryInfoA", "none"]
old-location: setup\msicreatetransformsummaryinfo.htm
tech.root: setup
ms.assetid: 7ed6738c-f693-477e-a3d7-e4f50d222fdb
ms.date: 12/05/2018
ms.keywords: MSITRANSFORM_ERROR_ADDEXISTINGROW, MSITRANSFORM_ERROR_ADDEXISTINGTABLE, MSITRANSFORM_ERROR_CHANGECODEPAGE, MSITRANSFORM_ERROR_DELMISSINGROW, MSITRANSFORM_ERROR_DELMISSINGTABLE, MSITRANSFORM_ERROR_UPDATEMISSINGROW, MSITRANSFORM_VALIDATE_LANGUAGE, MSITRANSFORM_VALIDATE_MAJORVERSION, MSITRANSFORM_VALIDATE_MINORVERSION, MSITRANSFORM_VALIDATE_NEWEQUALBASEVERSION, MSITRANSFORM_VALIDATE_NEWGREATERBASEVERSION, MSITRANSFORM_VALIDATE_NEWGREATEREQUALBASEVERSION, MSITRANSFORM_VALIDATE_NEWLESSBASEVERSION, MSITRANSFORM_VALIDATE_NEWLESSEQUALBASEVERSION, MSITRANSFORM_VALIDATE_PRODUCT, MSITRANSFORM_VALIDATE_UPDATEVERSION, MSITRANSFORM_VALIDATE_UPGRADECODE, MsiCreateTransformSummaryInfo, MsiCreateTransformSummaryInfo function, MsiCreateTransformSummaryInfoA, MsiCreateTransformSummaryInfoW, _msi_msicreatetransformsummaryinfo, msiquery/MsiCreateTransformSummaryInfo, msiquery/MsiCreateTransformSummaryInfoA, msiquery/MsiCreateTransformSummaryInfoW, none, setup.msicreatetransformsummaryinfo
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiCreateTransformSummaryInfoW (Unicode) and MsiCreateTransformSummaryInfoA (ANSI)
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
 - MsiCreateTransformSummaryInfoA
 - msiquery/MsiCreateTransformSummaryInfoA
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
 - MsiCreateTransformSummaryInfo
 - MsiCreateTransformSummaryInfoA
 - MsiCreateTransformSummaryInfoW
---

# MsiCreateTransformSummaryInfoA function


## -description

The 
<b>MsiCreateTransformSummaryInfo</b> function creates summary information of an existing transform to include validation and error conditions. Execution of this function sets the error record, which is accessible by using 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.

## -parameters

### -param hDatabase [in]

The handle to the database that contains the new database summary information.

### -param hDatabaseReference [in]

The handle to the database that contains the original summary information.

### -param szTransformFile [in]

The name of the transform to which the summary information is added.

### -param iErrorConditions [in]

The error conditions that should be suppressed when the transform is applied. Use one or more of the following values. 



<table>
<tr>
<th>Error condition</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="none"></a><a id="NONE"></a><dl>
<dt><b>none</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
None of the following conditions.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_ADDEXISTINGROW"></a><a id="msitransform_error_addexistingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_ADDEXISTINGROW</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Adding a row that  exists.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_DELMISSINGROW"></a><a id="msitransform_error_delmissingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_DELMISSINGROW</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Deleting a row that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_ADDEXISTINGTABLE"></a><a id="msitransform_error_addexistingtable"></a><dl>
<dt><b>MSITRANSFORM_ERROR_ADDEXISTINGTABLE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Adding a table that  exists.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_DELMISSINGTABLE"></a><a id="msitransform_error_delmissingtable"></a><dl>
<dt><b>MSITRANSFORM_ERROR_DELMISSINGTABLE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Deleting a table that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_UPDATEMISSINGROW"></a><a id="msitransform_error_updatemissingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_UPDATEMISSINGROW</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Updating a row that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_CHANGECODEPAGE"></a><a id="msitransform_error_changecodepage"></a><dl>
<dt><b>MSITRANSFORM_ERROR_CHANGECODEPAGE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Transform and database code pages do not match, and their code pages are neutral.

</td>
</tr>
</table>

### -param iValidation [in]

Specifies the properties to be validated to verify that the transform can be applied to the database. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Validation flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="none"></a><a id="NONE"></a><dl>
<dt><b>none</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Do not validate properties.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_LANGUAGE"></a><a id="msitransform_validate_language"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_LANGUAGE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Default language must match base database.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_PRODUCT"></a><a id="msitransform_validate_product"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_PRODUCT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Product must match base database.

</td>
</tr>
</table>
 

Validate product version flags.

<table>
<tr>
<th>Validation flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_MAJORVERSION"></a><a id="msitransform_validate_majorversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_MAJORVERSION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Check major version only.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_MINORVERSION"></a><a id="msitransform_validate_minorversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_MINORVERSION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Check major and minor versions only.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_UPDATEVERSION"></a><a id="msitransform_validate_updateversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_UPDATEVERSION</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Check major, minor, and update versions.

</td>
</tr>
</table>
 

Product version relationship flags. In the following table the installed version is the version of the package that is being transformed, and the base version is the version of the package that is used to create the transform.

<table>
<tr>
<th>Validation flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_NEWLESSBASEVERSION"></a><a id="msitransform_validate_newlessbaseversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_NEWLESSBASEVERSION</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Installed version &lt; base version.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_NEWLESSEQUALBASEVERSION"></a><a id="msitransform_validate_newlessequalbaseversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_NEWLESSEQUALBASEVERSION</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Installed version &lt;= base version.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_NEWEQUALBASEVERSION"></a><a id="msitransform_validate_newequalbaseversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_NEWEQUALBASEVERSION</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Installed version = base version.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_NEWGREATEREQUALBASEVERSION"></a><a id="msitransform_validate_newgreaterequalbaseversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_NEWGREATEREQUALBASEVERSION</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Installed version &gt;= base version.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_NEWGREATERBASEVERSION"></a><a id="msitransform_validate_newgreaterbaseversion"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_NEWGREATERBASEVERSION</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Installed version &gt; base version.

</td>
</tr>
</table>
 

Upgrade code validation flags.

<table>
<tr>
<th>Validation flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_VALIDATE_UPGRADECODE"></a><a id="msitransform_validate_upgradecode"></a><dl>
<dt><b>MSITRANSFORM_VALIDATE_UPGRADECODE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
UpgradeCode must match base database.

</td>
</tr>
</table>

## -returns

This function returns UINT.

## -remarks

The <a href="/windows/desktop/Msi/productcode">ProductCode</a> Property and 
<a href="/windows/desktop/Msi/productversion">ProductVersion</a> Property  must be defined in the 
<a href="/windows/desktop/Msi/property-table">Property Table</a> of both the base and reference databases. If MSITRANSFORM_VALIDATE_UPGRADECODE is used, the 
<a href="/windows/desktop/Msi/upgradecode">UpgradeCode</a> Property must also be defined in both databases. If these conditions are not met, 
<b>MsiCreateTransformSummaryInfo</b> returns ERROR_INSTALL_PACKAGE_INVALID.

<ul>
<li>Do not use the semicolon for filenames or paths, because it is used as a list delimiter for transforms, sources, and patches.</li>
<li>This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.</li>
</ul>




> [!NOTE]
> The msiquery.h header defines MsiCreateTransformSummaryInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-transforms">Database Transforms</a>



<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>
