---
UID: NS:winnt._OSVERSIONINFOA
title: OSVERSIONINFOA (winnt.h)
description: Contains operating system version information. (ANSI)
helpviewer_keywords: ["*LPOSVERSIONINFOA","*POSVERSIONINFOA","OSVERSIONINFO","OSVERSIONINFO structure","OSVERSIONINFOA","OSVERSIONINFOW","VER_PLATFORM_WIN32_NT","_OSVERSIONINFOA","_OSVERSIONINFOW","_win32_osversioninfo_str","base.osversioninfo_str","winnt/OSVERSIONINFO","winnt/OSVERSIONINFOA","winnt/OSVERSIONINFOW"]
old-location: base\osversioninfo_str.htm
tech.root: winprog
ms.assetid: a173df17-dad2-4330-aa66-4ff789fd7cc2
ms.date: 12/05/2018
ms.keywords: '*LPOSVERSIONINFOA, *POSVERSIONINFOA, OSVERSIONINFO, OSVERSIONINFO structure, OSVERSIONINFOA, OSVERSIONINFOW, VER_PLATFORM_WIN32_NT, _OSVERSIONINFOA, _OSVERSIONINFOW, _win32_osversioninfo_str, base.osversioninfo_str, winnt/OSVERSIONINFO, winnt/OSVERSIONINFOA, winnt/OSVERSIONINFOW'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OSVERSIONINFOW (Unicode) and OSVERSIONINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OSVERSIONINFOA, *POSVERSIONINFOA, *LPOSVERSIONINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OSVERSIONINFOA
 - winnt/_OSVERSIONINFOA
 - POSVERSIONINFOA
 - winnt/POSVERSIONINFOA
 - OSVERSIONINFOA
 - winnt/OSVERSIONINFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - OSVERSIONINFO
 - OSVERSIONINFOA
 - OSVERSIONINFOW
---

# OSVERSIONINFOA structure


## -description

Contains operating system version information. The information includes major and minor version numbers, a build number, a platform identifier, and descriptive text about the operating system. This structure is used with the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a> function.

To obtain additional version information, use the <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a> structure with <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a> instead.

## -struct-fields

### -field dwOSVersionInfoSize

The size of this data structure, in bytes. Set this member to <code>sizeof(OSVERSIONINFO)</code>.

### -field dwMajorVersion

The major version number of the operating system. For more information, see Remarks.

### -field dwMinorVersion

The minor version number of the operating system. For more information, see Remarks.

### -field dwBuildNumber

The build number of the operating system.

### -field dwPlatformId

The operating system platform. This member can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORM_WIN32_NT"></a><a id="ver_platform_win32_nt"></a><dl>
<dt><b>VER_PLATFORM_WIN32_NT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The operating system is Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, or Windows 2000.

</td>
</tr>
</table>

### -field szCSDVersion

A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system. If no Service Pack has been installed, the string is empty.

## -remarks

Relying on version information is not the best way to test for a feature. Instead, refer to the documentation for the feature of interest. For more information on common techniques for feature detection, see 
<a href="/windows/desktop/SysInfo/operating-system-version">Operating System Version</a>.

If you must require a particular operating system, be sure to use it as a minimum supported version, rather than design the test for the one operating system. This way, your detection code will continue to work on future versions of Windows.

The following table summarizes the values returned by supported versions of Windows. Use the information in the  column labeled "Other" to distinguish between operating systems with identical version numbers.

<table>
<tr>
<th>Operating system</th>
<th>Version number</th>
<th><b>dwMajorVersion</b></th>
<th><b>dwMinorVersion</b></th>
<th>Other</th>
</tr>
<tr>
<td>Windows 10</td>
<td>10.0*</td>
<td>10</td>
<td>0</td>
<td>OSVERSIONINFOEX.wProductType == VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Server 2016</td>
<td>10.0*</td>
<td>10</td>
<td>0</td>
<td>OSVERSIONINFOEX.wProductType != VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows 8.1</td>
<td>6.3*</td>
<td>6</td>
<td>3</td>
<td>OSVERSIONINFOEX.wProductType == VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Server 2012 R2</td>
<td>6.3*</td>
<td>6</td>
<td>3</td>
<td>OSVERSIONINFOEX.wProductType != VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows 8</td>
<td>6.2</td>
<td>6</td>
<td>2</td>
<td>OSVERSIONINFOEX.wProductType == VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Server 2012</td>
<td>6.2</td>
<td>6</td>
<td>2</td>
<td>OSVERSIONINFOEX.wProductType != VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows 7</td>
<td>6.1</td>
<td>6</td>
<td>1</td>
<td>OSVERSIONINFOEX.wProductType == VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Server 2008 R2</td>
<td>6.1</td>
<td>6</td>
<td>1</td>
<td>OSVERSIONINFOEX.wProductType != VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Server 2008</td>
<td>6.0</td>
<td>6</td>
<td>0</td>
<td>OSVERSIONINFOEX.wProductType != VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Vista</td>
<td>6.0</td>
<td>6</td>
<td>0</td>
<td>OSVERSIONINFOEX.wProductType == VER_NT_WORKSTATION</td>
</tr>
<tr>
<td>Windows Server 2003 R2</td>
<td>5.2</td>
<td>5</td>
<td>2</td>
<td>GetSystemMetrics(SM_SERVERR2) != 0</td>
</tr>
<tr>
<td>Windows Server 2003</td>
<td>5.2</td>
<td>5</td>
<td>2</td>
<td>GetSystemMetrics(SM_SERVERR2) == 0</td>
</tr>
<tr>
<td>Windows XP</td>
<td>5.1</td>
<td>5</td>
<td>1</td>
<td>Not applicable</td>
</tr>
<tr>
<td>Windows 2000</td>
<td>5.0</td>
<td>5</td>
<td>0</td>
<td>Not applicable</td>
</tr>
<tr>
<td colspan="5">
<b>*</b> For applications that have been manifested for Windows 8.1 or Windows 10. Applications not manifested for Windows 8.1 or Windows 10 will return the Windows 8 OS version value (6.2). To manifest your applications for Windows 8.1 or Windows 10, refer to <a href="/windows/desktop/SysInfo/targeting-your-application-at-windows-8-1">Targeting your application for Windows</a>.

</td>
</tr>
</table>
 


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.

<div class="code"></div>




> [!NOTE]
> The winnt.h header defines OSVERSIONINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a>



<a href="/windows/desktop/SysInfo/version-helper-apis">Version Helper APIs</a>
