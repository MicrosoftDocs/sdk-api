---
UID: NF:shlwapi.SHFormatDateTimeW
title: SHFormatDateTimeW function (shlwapi.h)
description: SHFormatDateTime may be altered or unavailable. (Unicode)
helpviewer_keywords: ["FDTF_DEFAULT", "FDTF_LONGDATE", "FDTF_LONGTIME", "FDTF_LTRDATE", "FDTF_NOAUTOREADINGORDER", "FDTF_RELATIVE", "FDTF_RTLDATE", "FDTF_SHORTDATE", "FDTF_SHORTTIME", "SHFormatDateTime", "SHFormatDateTime function [Windows Shell]", "SHFormatDateTimeW", "_win32_SHFormatDateTime", "shell.SHFormatDateTime", "shlwapi/SHFormatDateTime", "shlwapi/SHFormatDateTimeW"]
old-location: shell\SHFormatDateTime.htm
tech.root: shell
ms.assetid: 2208ed29-6029-4051-bdcc-885c42fe5c1b
ms.date: 12/05/2018
ms.keywords: FDTF_DEFAULT, FDTF_LONGDATE, FDTF_LONGTIME, FDTF_LTRDATE, FDTF_NOAUTOREADINGORDER, FDTF_RELATIVE, FDTF_RTLDATE, FDTF_SHORTDATE, FDTF_SHORTTIME, SHFormatDateTime, SHFormatDateTime function [Windows Shell], SHFormatDateTimeA, SHFormatDateTimeW, _win32_SHFormatDateTime, shell.SHFormatDateTime, shlwapi/SHFormatDateTime, shlwapi/SHFormatDateTimeA, shlwapi/SHFormatDateTimeW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHFormatDateTimeW (Unicode) and SHFormatDateTimeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHFormatDateTimeW
 - shlwapi/SHFormatDateTimeW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - SHFormatDateTime
 - SHFormatDateTimeA
 - SHFormatDateTimeW
---

# SHFormatDateTimeW function


## -description

<p class="CCE_Message">[<b>SHFormatDateTime</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Produces a string representation of a time specified as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -parameters

### -param pft [in]

Type: <b>const FILETIME UNALIGNED*</b>

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure whose time is to be converted to a string.

### -param pdwFlags [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that contains bitwise flags that specify the date and time format.




When you call the function, you can combine zero or more of the following flags, with exceptions as noted. You can also set this parameter to <b>NULL</b>, in which case the function assumes that the FDTF_DEFAULT flag is set.







#### FDTF_SHORTTIME (0x00000001)

0x00000001. Formats the time of day as specified by the <b>Regional and Language Options</b> application in Control Panel, but without seconds. This flag cannot be combined with FDTF_LONGTIME.

The short time was successfully formatted.



#### FDTF_SHORTDATE (0x00000002)

0x00000002. Formats the date as specified by the short date format in the <b>Regional and Language Options</b> application in Control Panel.  This flag cannot be combined with FDTF_LONGDATE.

The short date was successfully formatted.



#### FDTF_DEFAULT

Equivalent to FDTF_SHORTDATE | FDTF_SHORTTIME.



#### FDTF_LONGDATE (0x00000004)

0x00000004. Formats the date as specified by the long date format in the <b>Regional and Language Options</b> application in Control Panel. This flag cannot be combined with FDTF_SHORTDATE.

The long date was successfully formatted.



#### FDTF_LONGTIME (0x00000008)

0x00000008. Formats the time of day as specified by the <b>Regional and Language Options</b> application in Control Panel, including seconds. This flag cannot be combined with FDTF_SHORTTIME.

The long time was successfully formatted.



#### FDTF_RELATIVE (0x00000010)

0x00000010. If the FDTF_LONGDATE flag is set and the date in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure is the same date that <b>SHFormatDateTime</b> is called, then the day of the week (if present) is changed to "Today". If the date in the structure is the previous day, then the day of the week (if present) is changed to "Yesterday".

Relative notation was used for the date.



#### FDTF_LTRDATE (0x00000100)

0x00000100. Adds marks for left-to-right reading layout. This flag cannot be combined with FDTF_RTLDATE.



#### FDTF_RTLDATE (0x00000200)

0x00000200. Adds marks for right-to-left reading layout. This flag cannot be combined with FDTF_LTRDATE.



#### FDTF_NOAUTOREADINGORDER (0x00000400)

0x00000400. No reading order marks are inserted. Normally, in the absence of the FDTF_LTRDATE or FDTF_RTLDATE flag, <b>SHFormatDateTime</b> determines the reading order from the user's default locale, inserts reading order marks, and updates the <i>pdwFlags</i> output value appropriately. This flag prevents that process from occurring. It is used most commonly by legacy callers of <b>SHFormatDateTime</b>. This flag cannot be combined with FDTF_RTLDATE or FDTF_LTRDATE.

<b>Windows Server 2003 and Windows XP:  </b>This value is not available.


When the function returns, the <b>DWORD</b> value pointed to by this parameter can contain zero or more of the following flags.





#### FDTF_SHORTTIME (0x00000001)

0x00000001. Formats the time of day as specified by the <b>Regional and Language Options</b> application in Control Panel, but without seconds. This flag cannot be combined with FDTF_LONGTIME.

The short time was successfully formatted.



#### FDTF_SHORTDATE (0x00000002)

0x00000002. Formats the date as specified by the short date format in the <b>Regional and Language Options</b> application in Control Panel.  This flag cannot be combined with FDTF_LONGDATE.

The short date was successfully formatted.



#### FDTF_LONGDATE (0x00000004)

0x00000004. Formats the date as specified by the long date format in the <b>Regional and Language Options</b> application in Control Panel. This flag cannot be combined with FDTF_SHORTDATE.

The long date was successfully formatted.



#### FDTF_LONGTIME (0x00000008)

0x00000008. Formats the time of day as specified by the <b>Regional and Language Options</b> application in Control Panel, including seconds. This flag cannot be combined with FDTF_SHORTTIME.

The long time was successfully formatted.



#### FDTF_RELATIVE (0x00000010)

0x00000010. If the FDTF_LONGDATE flag is set and the date in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure is the same date that <b>SHFormatDateTime</b> is called, then the day of the week (if present) is changed to "Today". If the date in the structure is the previous day, then the day of the week (if present) is changed to "Yesterday".

Relative notation was used for the date.

### -param pszBuf [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that receives the formatted date and time. The buffer must be large enough to contain the number of TCHAR characters specified by the <i>cchBuf</i> parameter, including a terminating null character.

### -param cchBuf

Type: <b>UINT</b>

The number of TCHARs that can be contained by the buffer pointed to by <i>pszBuf</i>.


##### - pdwFlags.FDTF_DEFAULT

Equivalent to FDTF_SHORTDATE | FDTF_SHORTTIME.


##### - pdwFlags.FDTF_LTRDATE (0x00000100)

0x00000100. Adds marks for left-to-right reading layout. This flag cannot be combined with FDTF_RTLDATE.


##### - pdwFlags.FDTF_NOAUTOREADINGORDER (0x00000400)

0x00000400. No reading order marks are inserted. Normally, in the absence of the FDTF_LTRDATE or FDTF_RTLDATE flag, <b>SHFormatDateTime</b> determines the reading order from the user's default locale, inserts reading order marks, and updates the <i>pdwFlags</i> output value appropriately. This flag prevents that process from occurring. It is used most commonly by legacy callers of <b>SHFormatDateTime</b>. This flag cannot be combined with FDTF_RTLDATE or FDTF_LTRDATE.

<b>Windows Server 2003 and Windows XP:  </b>This value is not available.


##### - pdwFlags.FDTF_RTLDATE (0x00000200)

0x00000200. Adds marks for right-to-left reading layout. This flag cannot be combined with FDTF_LTRDATE.

## -returns

Type: <b>int</b>

Returns the number of TCHARs written to the buffer, including the terminating null character. On failure, this value is 0.

## -see-also

<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata">GetTimeFormat</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines SHFormatDateTime as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
