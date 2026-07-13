---
UID: NF:msiquery.MsiViewGetErrorA
title: MsiViewGetErrorA function (msiquery.h)
description: The MsiViewGetError function returns the error that occurred in the MsiViewModify function. (ANSI)
helpviewer_keywords: ["MsiViewGetErrorA", "msiquery/MsiViewGetErrorA"]
old-location: setup\msiviewgeterror.htm
tech.root: setup
ms.assetid: a59ab850-204b-40b7-bf24-d6a2d7ae82f4
ms.date: 12/05/2018
ms.keywords: MsiViewGetError, MsiViewGetError function, MsiViewGetErrorA, MsiViewGetErrorW, _msi_msiviewgeterror, msiquery/MsiViewGetError, msiquery/MsiViewGetErrorA, msiquery/MsiViewGetErrorW, setup.msiviewgeterror
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0  or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiViewGetErrorW (Unicode) and MsiViewGetErrorA (ANSI)
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
 - MsiViewGetErrorA
 - msiquery/MsiViewGetErrorA
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
 - MsiViewGetError
 - MsiViewGetErrorA
 - MsiViewGetErrorW
---

# MsiViewGetErrorA function


## -description

The 
<b>MsiViewGetError</b> function returns the error that occurred in the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewmodify">MsiViewModify</a> function.

## -parameters

### -param hView [in]

Handle to the view.

### -param szColumnNameBuffer [out]

Pointer to the buffer that receives the null-terminated column name. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szColumnName</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns MSIDBERROR_MOREDATA and <i>pcchBuf</i> contains the required buffer size in TCHARs, not including the terminating null character. On return of MSIDBERROR_NOERROR, <i>pcchBuf</i> contains the number of TCHARs written to the buffer, not including the terminating null character. This parameter is an empty string if there are no errors.

### -param pcchBuf [in, out]

Pointer to the variable that specifies the size, in TCHARs, of the buffer pointed to by the variable <i>szColumnNameBuffer</i>. When the function returns MSIDBERROR_NOERROR, this variable contains the size of the data copied to <i>szColumnNameBuffer</i>, not including the terminating null character. If <i>szColumnNameBuffer</i> is not large enough, the function returns MSIDBERROR_MOREDATA and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchBuf</i>.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer was too small to receive data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_FUNCTIONERROR</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_NOERROR</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully with no errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_DUPLICATEKEY</b></dt>
</dl>
</td>
<td width="60%">
The new record duplicates primary keys of the existing record in a table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
There are no null values allowed; or the column is about to be deleted, but is referenced by another row.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADLINK</b></dt>
</dl>
</td>
<td width="60%">
The corresponding record in a foreign table was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data is greater than the maximum value allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_UNDERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data is less than the minimum value allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_NOTINSET</b></dt>
</dl>
</td>
<td width="60%">
The data is not a member of the values permitted in the set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADVERSION</b></dt>
</dl>
</td>
<td width="60%">
An invalid version string was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADCASE</b></dt>
</dl>
</td>
<td width="60%">
The case was invalid. The case must be all uppercase or all lowercase.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADGUID</b></dt>
</dl>
</td>
<td width="60%">
An invalid GUID was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADWILDCARD</b></dt>
</dl>
</td>
<td width="60%">
An invalid wildcard file name was supplied, or the use of wildcards was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADIDENTIFIER</b></dt>
</dl>
</td>
<td width="60%">
An invalid identifier was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADLANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Invalid language IDs were supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADFILENAME</b></dt>
</dl>
</td>
<td width="60%">
An invalid file name was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADPATH</b></dt>
</dl>
</td>
<td width="60%">
An invalid path was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADCONDITION</b></dt>
</dl>
</td>
<td width="60%">
An invalid conditional statement was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADFORMATTED</b></dt>
</dl>
</td>
<td width="60%">
An invalid format string was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADTEMPLATE</b></dt>
</dl>
</td>
<td width="60%">
An invalid template string was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADDEFAULTDIR</b></dt>
</dl>
</td>
<td width="60%">
An invalid string was supplied in the DefaultDir column of the 
<a href="/windows/desktop/Msi/directory-table">Directory</a> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADREGPATH</b></dt>
</dl>
</td>
<td width="60%">
An invalid registry path string was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADCUSTOMSOURCE</b></dt>
</dl>
</td>
<td width="60%">
An invalid string was supplied in the CustomSource column of the 
<a href="/windows/desktop/Msi/customaction-table">CustomAction</a> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADPROPERTY</b></dt>
</dl>
</td>
<td width="60%">
An invalid property string was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_MISSINGDATA</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="/windows/desktop/Msi/-validation-table">_Validation</a> table is missing a reference to a column.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADCATEGORY</b></dt>
</dl>
</td>
<td width="60%">
The category column of the <a href="/windows/desktop/Msi/-validation-table">_Validation</a> table for the column is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADCABINET</b></dt>
</dl>
</td>
<td width="60%">
An invalid cabinet name was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADKEYTABLE</b></dt>
</dl>
</td>
<td width="60%">
The table in the Keytable column of the <a href="/windows/desktop/Msi/-validation-table">_Validation</a> table was not found or loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADMAXMINVALUES</b></dt>
</dl>
</td>
<td width="60%">
The value in the MaxValue column of the <a href="/windows/desktop/Msi/-validation-table">_Validation</a> table is less than the value in the MinValue column.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADSHORTCUT</b></dt>
</dl>
</td>
<td width="60%">
An invalid shortcut target name was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_STRINGOVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The string is too long for the length specified by the column definition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MSIDBERROR_BADLOCALIZEATTRIB</b></dt>
</dl>
</td>
<td width="60%">
An invalid localization attribute was supplied. (Primary keys cannot be localized.)

</td>
</tr>
</table>
 


<div> </div>


Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.

## -remarks

You should only call the 
<b>MsiViewGetError</b> function when 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewmodify">MsiViewModify</a> returns ERROR_INVALID_DATA, indicating that the data is invalid. Errors are only recorded for MSIMODIFY_VALIDATE, MSIMODIFY_VALIDATE_NEW, and MSIMODIFY_VALIDATEFIELD.

If ERROR_MORE_DATA is returned, the parameter that  is a pointer gives the size of the buffer required to hold the string. Upon success, it gives the number of characters written to the string buffer. Therefore you can get the required size of the buffer by passing a small buffer (one character minimum) and examining the value at <i>pcchPathBuf</i> when the function returns MSIDBERROR_MOREDATA. Do not attempt to determine the size of the buffer by passing in null as <i>szColumnNameBuffer</i> or a buffer size of 0 in the <b>DWORD</b> referenced by <i>pcchBuf</i>.

Once MSIDBERROR_NOERROR is returned, no more validation errors remain. The MSIDBERROR return value indicates the type of validation error that occurred for the value located in the column identified by the <i>szColumnNameBuffer</i>.





> [!NOTE]
> The msiquery.h header defines MsiViewGetError as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>



<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>
