---
UID: NF:msi.MsiEnableLogA
title: MsiEnableLogA function (msi.h)
description: The MsiEnableLog function sets the log mode for all subsequent installations that are initiated in the calling process. (ANSI)
helpviewer_keywords: ["INSTALLLOGATTRIBUTES_APPEND", "INSTALLLOGATTRIBUTES_FLUSHEACHLINE", "INSTALLLOGMODE_ACTIONDATA", "INSTALLLOGMODE_ACTIONSTART", "INSTALLLOGMODE_COMMONDATA", "INSTALLLOGMODE_ERROR", "INSTALLLOGMODE_EXTRADEBUG", "INSTALLLOGMODE_FATALEXIT", "INSTALLLOGMODE_INFO", "INSTALLLOGMODE_LOGONLYONERROR", "INSTALLLOGMODE_OUTOFDISKSPACE", "INSTALLLOGMODE_PROPERTYDUMP", "INSTALLLOGMODE_RESOLVESOURCE", "INSTALLLOGMODE_USER", "INSTALLLOGMODE_VERBOSE", "INSTALLLOGMODE_WARNING", "MsiEnableLogA", "msi/MsiEnableLogA"]
old-location: setup\msienablelog.htm
tech.root: setup
ms.assetid: 117ccd0b-e434-453f-9602-ff50bc85db6e
ms.date: 12/05/2018
ms.keywords: INSTALLLOGATTRIBUTES_APPEND, INSTALLLOGATTRIBUTES_FLUSHEACHLINE, INSTALLLOGMODE_ACTIONDATA, INSTALLLOGMODE_ACTIONSTART, INSTALLLOGMODE_COMMONDATA, INSTALLLOGMODE_ERROR, INSTALLLOGMODE_EXTRADEBUG, INSTALLLOGMODE_FATALEXIT, INSTALLLOGMODE_INFO, INSTALLLOGMODE_LOGONLYONERROR, INSTALLLOGMODE_OUTOFDISKSPACE, INSTALLLOGMODE_PROPERTYDUMP, INSTALLLOGMODE_RESOLVESOURCE, INSTALLLOGMODE_USER, INSTALLLOGMODE_VERBOSE, INSTALLLOGMODE_WARNING, MsiEnableLog, MsiEnableLog function, MsiEnableLogA, MsiEnableLogW, _msi_msienablelog, msi/MsiEnableLog, msi/MsiEnableLogA, msi/MsiEnableLogW, setup.msienablelog
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnableLogW (Unicode) and MsiEnableLogA (ANSI)
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
 - MsiEnableLogA
 - msi/MsiEnableLogA
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
 - MsiEnableLog
 - MsiEnableLogA
 - MsiEnableLogW
---

# MsiEnableLogA function


## -description

The 
<b>MsiEnableLog</b> function sets the log mode for all subsequent installations that are initiated in the calling process.

## -parameters

### -param dwLogMode [in]

Specifies the log mode. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_FATALEXIT"></a><a id="installlogmode_fatalexit"></a><dl>
<dt><b>INSTALLLOGMODE_FATALEXIT</b></dt>
</dl>
</td>
<td width="60%">
Logs out of memory or fatal exit information.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_ERROR"></a><a id="installlogmode_error"></a><dl>
<dt><b>INSTALLLOGMODE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Logs the error messages.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_EXTRADEBUG"></a><a id="installlogmode_extradebug"></a><dl>
<dt><b>INSTALLLOGMODE_EXTRADEBUG</b></dt>
</dl>
</td>
<td width="60%">
Sends extra debugging information, such as handle creation information, to the log file. 

<b>Windows 2000 and Windows XP:  </b>This feature is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_WARNING"></a><a id="installlogmode_warning"></a><dl>
<dt><b>INSTALLLOGMODE_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Logs the warning messages.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_USER"></a><a id="installlogmode_user"></a><dl>
<dt><b>INSTALLLOGMODE_USER</b></dt>
</dl>
</td>
<td width="60%">
Logs the user requests.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_INFO"></a><a id="installlogmode_info"></a><dl>
<dt><b>INSTALLLOGMODE_INFO</b></dt>
</dl>
</td>
<td width="60%">
Logs the status messages that are not displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_RESOLVESOURCE"></a><a id="installlogmode_resolvesource"></a><dl>
<dt><b>INSTALLLOGMODE_RESOLVESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Request to determine a valid source location.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_OUTOFDISKSPACE"></a><a id="installlogmode_outofdiskspace"></a><dl>
<dt><b>INSTALLLOGMODE_OUTOFDISKSPACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates insufficient disk space.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_ACTIONSTART"></a><a id="installlogmode_actionstart"></a><dl>
<dt><b>INSTALLLOGMODE_ACTIONSTART</b></dt>
</dl>
</td>
<td width="60%">
Logs the start of new installation actions.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_ACTIONDATA"></a><a id="installlogmode_actiondata"></a><dl>
<dt><b>INSTALLLOGMODE_ACTIONDATA</b></dt>
</dl>
</td>
<td width="60%">
Logs the data record with the installation action.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_COMMONDATA"></a><a id="installlogmode_commondata"></a><dl>
<dt><b>INSTALLLOGMODE_COMMONDATA</b></dt>
</dl>
</td>
<td width="60%">
Logs the parameters for user-interface initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_PROPERTYDUMP"></a><a id="installlogmode_propertydump"></a><dl>
<dt><b>INSTALLLOGMODE_PROPERTYDUMP</b></dt>
</dl>
</td>
<td width="60%">
Logs the property values at termination.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_VERBOSE"></a><a id="installlogmode_verbose"></a><dl>
<dt><b>INSTALLLOGMODE_VERBOSE</b></dt>
</dl>
</td>
<td width="60%">
Logs the information in all the other log modes, except for <b>INSTALLLOGMODE_EXTRADEBUG</b>. This sends large amounts of information to a log file not generally useful to users. May be used for technical support.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGMODE_LOGONLYONERROR"></a><a id="installlogmode_logonlyonerror"></a><dl>
<dt><b>INSTALLLOGMODE_LOGONLYONERROR</b></dt>
</dl>
</td>
<td width="60%">
Logging information is collected but is less frequently saved to the log file. This can improve the performance of some installations, but may have little benefit for large installations. The log file is removed when the installation succeeds. If the installation fails, all logging information is saved to the log file. 

<b>Windows Installer 2.0:  </b>This log mode is not available.

</td>
</tr>
</table>

### -param szLogFile [in]

Specifies the string that holds the full path to the log file. Entering a null disables logging, in which case <i>dwlogmode</i> is ignored. If a path is supplied, then <i>dwlogmode</i> must not be zero.

### -param dwLogAttributes [in]

Specifies how frequently the log buffer is to be flushed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGATTRIBUTES_APPEND"></a><a id="installlogattributes_append"></a><dl>
<dt><b>INSTALLLOGATTRIBUTES_APPEND</b></dt>
</dl>
</td>
<td width="60%">
If this value is set, the installer appends the existing log specified by <i>szLogFile</i>. If not set, any existing log specified by <i>szLogFile</i> is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLLOGATTRIBUTES_FLUSHEACHLINE"></a><a id="installlogattributes_flusheachline"></a><dl>
<dt><b>INSTALLLOGATTRIBUTES_FLUSHEACHLINE</b></dt>
</dl>
</td>
<td width="60%">
Forces the log buffer to be flushed after each line. If this value is not set, the installer flushes the log buffer after 20 lines by calling 
<a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a>.

</td>
</tr>
</table>

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid log mode was specified.

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
</table>

## -remarks

For a description of the Logging policy, see 
<a href="/windows/desktop/Msi/system-policy">System Policy</a>.

The path to the log file location must already exist when using this function. The Installer does not create the directory structure for the log file.





> [!NOTE]
> The msi.h header defines MsiEnableLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Interface and Logging Functions</a>



<a href="/windows/desktop/Msi/logging">Logging</a>
