---
UID: NF:msiquery.MsiRecordGetStringW
title: MsiRecordGetStringW function (msiquery.h)
description: The MsiRecordGetString function returns the string value of a record field. (Unicode)
helpviewer_keywords: ["MsiRecordGetString", "MsiRecordGetString function", "MsiRecordGetStringW", "_msi_msirecordgetstring", "msiquery/MsiRecordGetString", "msiquery/MsiRecordGetStringW", "setup.msirecordgetstring"]
old-location: setup\msirecordgetstring.htm
tech.root: setup
ms.assetid: 4d1b049c-9511-4858-8cc1-3cd2424c55ca
ms.date: 12/05/2018
ms.keywords: MsiRecordGetString, MsiRecordGetString function, MsiRecordGetStringA, MsiRecordGetStringW, _msi_msirecordgetstring, msiquery/MsiRecordGetString, msiquery/MsiRecordGetStringA, msiquery/MsiRecordGetStringW, setup.msirecordgetstring
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiRecordGetStringW (Unicode) and MsiRecordGetStringA (ANSI)
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
 - MsiRecordGetStringW
 - msiquery/MsiRecordGetStringW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiRecordGetString
 - MsiRecordGetStringA
 - MsiRecordGetStringW
---

# MsiRecordGetStringW function


## -description

The 
<b>MsiRecordGetString</b> function returns the string value of a record field.

## -parameters

### -param hRecord [in]

Handle to the record.

### -param iField [in]

Specifies the field requested.

### -param szValueBuf [out]

Pointer to the buffer that receives the null terminated string containing the value of the record field. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szValueBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns <b>ERROR_MORE_DATA</b> and <i>pcchValueBuf</i> contains the required buffer size in TCHARs, not including the terminating null character. On return of <b>ERROR_SUCCESS</b>, <i>pcchValueBuf</i> contains the number of <b>TCHARs</b> written to the buffer, not including the terminating null character.

### -param pcchValueBuf [in, out]

Pointer to the variable that specifies the size, in <b>TCHAR</b>s, of the buffer pointed to by the variable <i>szValueBuf</i>. When the function returns <b>ERROR_SUCCESS</b>, this variable contains the size of the data copied to <i>szValueBuf</i>, not including the terminating null character. If <i>szValueBuf</i> is not large enough, the function returns <b>ERROR_MORE_DATA</b> and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchValueBuf</i>.

## -returns

The 
<b>MsiRecordGetString</b> function returns one of the following values:

## -remarks

If <b>ERROR_MORE_DATA</b> is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If <b>ERROR_SUCCESS</b> is returned, it gives the number of characters written to the string buffer. To get the size of the buffer, pass in the address of a 1 character buffer as <i>szValueBuf</i> and specify the size of the buffer with <i>pcchValueBuf</i> as 0. This ensures that no string value returned by the function fits into the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).





> [!NOTE]
> The msiquery.h header defines MsiRecordGetString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>



<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>
