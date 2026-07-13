---
UID: NF:setupapi.SetupQueryFileLogW
title: SetupQueryFileLogW function (setupapi.h)
description: The SetupQueryFileLog function returns information from a setup file log. (Unicode)
helpviewer_keywords: ["SetupFileLogChecksum", "SetupFileLogDiskDescription", "SetupFileLogDiskTagfile", "SetupFileLogOtherInfo", "SetupFileLogSourceFile name", "SetupQueryFileLog", "SetupQueryFileLog function [Setup API]", "SetupQueryFileLogW", "_setupapi_setupqueryfilelog", "setup.setupqueryfilelog", "setupapi/SetupQueryFileLog", "setupapi/SetupQueryFileLogW"]
old-location: setup\setupqueryfilelog.htm
tech.root: setup
ms.assetid: c01233ee-4e3a-454b-b2e2-032937c874c9
ms.date: 12/05/2018
ms.keywords: SetupFileLogChecksum, SetupFileLogDiskDescription, SetupFileLogDiskTagfile, SetupFileLogOtherInfo, SetupFileLogSourceFile name, SetupQueryFileLog, SetupQueryFileLog function [Setup API], SetupQueryFileLogA, SetupQueryFileLogW, _setupapi_setupqueryfilelog, setup.setupqueryfilelog, setupapi/SetupQueryFileLog, setupapi/SetupQueryFileLogA, setupapi/SetupQueryFileLogW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueryFileLogW (Unicode) and SetupQueryFileLogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupQueryFileLogW
 - setupapi/SetupQueryFileLogW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupQueryFileLog
 - SetupQueryFileLogA
 - SetupQueryFileLogW
---

# SetupQueryFileLogW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryFileLog</b> function returns information from a setup file log.

## -parameters

### -param FileLogHandle [in]

Handle to the file log as returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitializefileloga">SetupInitializeFileLog</a>.

### -param LogSectionName [in]

Optional pointer to the section name for the log file in a format that is meaningful to the caller. You should use a <b>null</b>-terminated string. Required for non-system logs. If no <i>LogSectionName</i> is specified for a system log, a default is supplied.

### -param TargetFilename [in]

Name of the file for which log information is desired. You should use a <b>null</b>-terminated string.

### -param DesiredInfo [in]

Indicates what information should be returned to the <i>DataOut</i> buffer. This parameter can be one of the following enumerated values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SetupFileLogSourceFile_name"></a><a id="setupfilelogsourcefile_name"></a><a id="SETUPFILELOGSOURCEFILE_NAME"></a><dl>
<dt><b>SetupFileLogSourceFile name</b></dt>
</dl>
</td>
<td width="60%">
Name of the source file as it exists on the source media

</td>
</tr>
<tr>
<td width="40%"><a id="SetupFileLogChecksum"></a><a id="setupfilelogchecksum"></a><a id="SETUPFILELOGCHECKSUM"></a><dl>
<dt><b>SetupFileLogChecksum</b></dt>
</dl>
</td>
<td width="60%">
A  checksum value used by the system log

</td>
</tr>
<tr>
<td width="40%"><a id="SetupFileLogDiskTagfile"></a><a id="setupfilelogdisktagfile"></a><a id="SETUPFILELOGDISKTAGFILE"></a><dl>
<dt><b>SetupFileLogDiskTagfile</b></dt>
</dl>
</td>
<td width="60%">
Name of the tag file of the media source containing the source file

</td>
</tr>
<tr>
<td width="40%"><a id="SetupFileLogDiskDescription"></a><a id="setupfilelogdiskdescription"></a><a id="SETUPFILELOGDISKDESCRIPTION"></a><dl>
<dt><b>SetupFileLogDiskDescription</b></dt>
</dl>
</td>
<td width="60%">
The human-readable description of the media where the source file resides

</td>
</tr>
<tr>
<td width="40%"><a id="SetupFileLogOtherInfo"></a><a id="setupfilelogotherinfo"></a><a id="SETUPFILELOGOTHERINFO"></a><dl>
<dt><b>SetupFileLogOtherInfo</b></dt>
</dl>
</td>
<td width="60%">
Additional information associated with the logged file

</td>
</tr>
</table>
 

If the value of <i>DesiredInfo</i> is greater than <b>SetupFileLogOtherInfo</b> the function will fail, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INVALID_PARAMETER.

### -param DataOut [in, out]

Optional pointer to a buffer in which this function returns the requested information for the file. You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. See the Remarks section. Using this technique, you can avoid errors due to an insufficient buffer size. Not all information is provided for every file. An error is not returned if an empty entry for the file exists in the log. This parameter can be <b>NULL</b>.

### -param ReturnBufferSize [in]

Size of the <i>DataOut</i> buffer,  in characters. This includes the <b>null</b> terminator. If the buffer is too small and <i>DataOut</i> is specified, data is not stored in the buffer and the function returns zero. If <i>DataOut</i> is not specified, the <i>ReturnBufferSize</i> parameter is ignored.

### -param RequiredSize [in, out]

Optional pointer to a variable that receives the required size of <i>DataOut</i>, in characters. This number includes the <b>null</b> terminator.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called with a <i>DataOut</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the value of <i>DesiredInfo</i> is greater than <b>SetupFileLogOtherInfo</b> the function will fail, and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INVALID_PARAMETER.





> [!NOTE]
> The setupapi.h header defines SetupQueryFileLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuplogfilea">SetupLogFile</a>
