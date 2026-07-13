---
UID: NS:winnt._OSVERSIONINFOEXW
title: OSVERSIONINFOEXW (winnt.h)
description: Contains operating system version information. The information includes major and minor version numbers, a build number, a platform identifier, and information about product suites and the latest Service Pack installed on the system. (Unicode)
helpviewer_keywords: ["*LPOSVERSIONINFOEXW","*POSVERSIONINFOEXW","*PRTL_OSVERSIONINFOEXW","LPOSVERSIONINFOEX","LPOSVERSIONINFOEX structure pointer","OSVERSIONINFOEX","OSVERSIONINFOEX structure","OSVERSIONINFOEXA","OSVERSIONINFOEXW","POSVERSIONINFOEX","POSVERSIONINFOEX structure pointer","RTL_OSVERSIONINFOEXW","VER_NT_DOMAIN_CONTROLLER","VER_NT_SERVER","VER_NT_WORKSTATION","VER_SUITE_BACKOFFICE","VER_SUITE_BLADE","VER_SUITE_COMPUTE_SERVER","VER_SUITE_DATACENTER","VER_SUITE_EMBEDDEDNT","VER_SUITE_ENTERPRISE","VER_SUITE_MULTIUSERTS","VER_SUITE_PERSONAL","VER_SUITE_SINGLEUSERTS","VER_SUITE_SMALLBUSINESS","VER_SUITE_SMALLBUSINESS_RESTRICTED","VER_SUITE_STORAGE_SERVER","VER_SUITE_TERMINAL","VER_SUITE_WH_SERVER","_OSVERSIONINFOEXA","_OSVERSIONINFOEXW","_win32_osversioninfoex_str","base.osversioninfoex_str","winnt/LPOSVERSIONINFOEX","winnt/OSVERSIONINFOEX","winnt/OSVERSIONINFOEXA","winnt/OSVERSIONINFOEXW","winnt/POSVERSIONINFOEX"]
old-location: base\osversioninfoex_str.htm
tech.root: winprog
ms.assetid: 4ab07a72-404d-459b-b061-b3b06b5db37e
ms.date: 12/05/2018
ms.keywords: '*LPOSVERSIONINFOEXW, *POSVERSIONINFOEXW, *PRTL_OSVERSIONINFOEXW, LPOSVERSIONINFOEX, LPOSVERSIONINFOEX structure pointer, OSVERSIONINFOEX, OSVERSIONINFOEX structure, OSVERSIONINFOEXA, OSVERSIONINFOEXW, POSVERSIONINFOEX, POSVERSIONINFOEX structure pointer, RTL_OSVERSIONINFOEXW, VER_NT_DOMAIN_CONTROLLER, VER_NT_SERVER, VER_NT_WORKSTATION, VER_SUITE_BACKOFFICE, VER_SUITE_BLADE, VER_SUITE_COMPUTE_SERVER, VER_SUITE_DATACENTER, VER_SUITE_EMBEDDEDNT, VER_SUITE_ENTERPRISE, VER_SUITE_MULTIUSERTS, VER_SUITE_PERSONAL, VER_SUITE_SINGLEUSERTS, VER_SUITE_SMALLBUSINESS, VER_SUITE_SMALLBUSINESS_RESTRICTED, VER_SUITE_STORAGE_SERVER, VER_SUITE_TERMINAL, VER_SUITE_WH_SERVER, _OSVERSIONINFOEXA, _OSVERSIONINFOEXW, _win32_osversioninfoex_str, base.osversioninfoex_str, winnt/LPOSVERSIONINFOEX, winnt/OSVERSIONINFOEX, winnt/OSVERSIONINFOEXA, winnt/OSVERSIONINFOEXW, winnt/POSVERSIONINFOEX'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OSVERSIONINFOEXW (Unicode) and OSVERSIONINFOEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OSVERSIONINFOEXW, *POSVERSIONINFOEXW, *LPOSVERSIONINFOEXW, RTL_OSVERSIONINFOEXW, *PRTL_OSVERSIONINFOEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OSVERSIONINFOEXW
 - winnt/_OSVERSIONINFOEXW
 - POSVERSIONINFOEXW
 - winnt/POSVERSIONINFOEXW
 - OSVERSIONINFOEXW
 - winnt/OSVERSIONINFOEXW
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
 - OSVERSIONINFOEX
 - OSVERSIONINFOEXA
 - OSVERSIONINFOEXW
---

# OSVERSIONINFOEXW structure


## -description

Contains operating system version information. The information includes major and minor version 
    numbers, a build number, a platform identifier, and information about product suites and the latest Service Pack 
    installed on the system. This structure is used with the 
    <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a> and 
    <a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> functions.

## -struct-fields

### -field dwOSVersionInfoSize

The size of this data structure, in bytes. Set this member to 
      <code>sizeof(OSVERSIONINFOEX)</code>.

### -field dwMajorVersion

The major version number of the operating system. For more information, see Remarks.

### -field dwMinorVersion

The minor version number of the operating system. For more information, see Remarks.

### -field dwBuildNumber

The build number of the operating system.

### -field dwPlatformId

The operating system platform. This member can be <b>VER_PLATFORM_WIN32_NT</b> (2).

### -field szCSDVersion

A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack 
      installed on the system. If no Service Pack has been installed, the string is empty.

### -field wServicePackMajor

The major version number of the latest Service Pack installed on the system. For example, for Service Pack 
      3, the major version number is 3. If no Service Pack has been installed, the value is zero.

### -field wServicePackMinor

The minor version number of the latest Service Pack installed on the system. For example, for Service Pack 
      3, the minor version number is 0.

### -field wSuiteMask

A bit mask that identifies the product suites available on the system. This member can be a combination of 
      the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_BACKOFFICE"></a><a id="ver_suite_backoffice"></a><dl>
<dt><b>VER_SUITE_BACKOFFICE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Microsoft BackOffice components are installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_BLADE"></a><a id="ver_suite_blade"></a><dl>
<dt><b>VER_SUITE_BLADE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Web Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_COMPUTE_SERVER"></a><a id="ver_suite_compute_server"></a><dl>
<dt><b>VER_SUITE_COMPUTE_SERVER</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Compute Cluster Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_DATACENTER"></a><a id="ver_suite_datacenter"></a><dl>
<dt><b>VER_SUITE_DATACENTER</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or 
        Windows 2000 Datacenter Server is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_ENTERPRISE"></a><a id="ver_suite_enterprise"></a><dl>
<dt><b>VER_SUITE_ENTERPRISE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or 
        Windows 2000 Advanced Server is installed. Refer to the Remarks section for more information 
        about this bit flag.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_EMBEDDEDNT"></a><a id="ver_suite_embeddednt"></a><dl>
<dt><b>VER_SUITE_EMBEDDEDNT</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Windows XP Embedded is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_PERSONAL"></a><a id="ver_suite_personal"></a><dl>
<dt><b>VER_SUITE_PERSONAL</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Windows Vista Home Premium, Windows Vista Home Basic, or 
        Windows XP Home Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_SINGLEUSERTS"></a><a id="ver_suite_singleuserts"></a><dl>
<dt><b>VER_SUITE_SINGLEUSERTS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Remote Desktop is supported, but only one interactive session is supported. This value is set unless the 
        system is running in application server mode.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_SMALLBUSINESS"></a><a id="ver_suite_smallbusiness"></a><dl>
<dt><b>VER_SUITE_SMALLBUSINESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Microsoft Small Business Server was once installed on the system, but may have been upgraded to another 
        version of Windows. Refer to the Remarks section for more information about this bit flag.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></a><a id="ver_suite_smallbusiness_restricted"></a><dl>
<dt><b>VER_SUITE_SMALLBUSINESS_RESTRICTED</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Microsoft Small Business Server is installed with the restrictive client license in force. Refer to the 
        Remarks section for more information about this bit flag.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_STORAGE_SERVER"></a><a id="ver_suite_storage_server"></a><dl>
<dt><b>VER_SUITE_STORAGE_SERVER</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_TERMINAL"></a><a id="ver_suite_terminal"></a><dl>
<dt><b>VER_SUITE_TERMINAL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Terminal Services is installed. This value is always set.

If <b>VER_SUITE_TERMINAL</b> is set but <b>VER_SUITE_SINGLEUSERTS</b> 
         is not set, the system is running in application server mode.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_WH_SERVER"></a><a id="ver_suite_wh_server"></a><dl>
<dt><b>VER_SUITE_WH_SERVER</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Windows Home Server is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_MULTIUSERTS"></a><a id="ver_suite_multiuserts"></a><dl>
<dt><b>VER_SUITE_MULTIUSERTS</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
AppServer mode is enabled.

</td>
</tr>
</table>

### -field wProductType

Any additional information about the system. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_NT_DOMAIN_CONTROLLER"></a><a id="ver_nt_domain_controller"></a><dl>
<dt><b>VER_NT_DOMAIN_CONTROLLER</b></dt>
<dt>0x0000002</dt>
</dl>
</td>
<td width="60%">
The system is a domain controller and the operating system is Windows Server 2012 , Windows Server 2008 R2, Windows Server 2008, 
        Windows Server 2003, or Windows 2000 Server.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_NT_SERVER"></a><a id="ver_nt_server"></a><dl>
<dt><b>VER_NT_SERVER</b></dt>
<dt>0x0000003</dt>
</dl>
</td>
<td width="60%">
The operating system is  Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, Windows Server 2003, or 
         Windows 2000 Server.

Note that a server that is also a domain controller is reported as 
         <b>VER_NT_DOMAIN_CONTROLLER</b>, not <b>VER_NT_SERVER</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_NT_WORKSTATION"></a><a id="ver_nt_workstation"></a><dl>
<dt><b>VER_NT_WORKSTATION</b></dt>
<dt>0x0000001</dt>
</dl>
</td>
<td width="60%">
The operating system is Windows 8, Windows 7, Windows Vista, Windows XP Professional, 
        Windows XP Home Edition, or Windows 2000 Professional.

</td>
</tr>
</table>

### -field wReserved

Reserved for future use.

## -remarks

Relying on version information is not the best way to test for a feature. Instead, refer to the documentation 
    for the feature of interest. For more information on common techniques for feature detection, see 
    <a href="/windows/desktop/SysInfo/operating-system-version">Operating System Version</a>.

If you must require a particular operating system, be sure to use it as a minimum supported version, rather 
    than design the test for the one operating system. This way, your detection code will continue to work on future 
    versions of Windows.

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
<td>Windows Home Server</td>
<td>5.2</td>
<td>5</td>
<td>2</td>
<td>OSVERSIONINFOEX.wSuiteMask &amp; VER_SUITE_WH_SERVER</td>
</tr>
<tr>
<td>Windows Server 2003</td>
<td>5.2</td>
<td>5</td>
<td>2</td>
<td>GetSystemMetrics(SM_SERVERR2) == 0</td>
</tr>
<tr>
<td>Windows XP Professional x64 Edition</td>
<td>5.2</td>
<td>5</td>
<td>2</td>
<td>(OSVERSIONINFOEX.wProductType == VER_NT_WORKSTATION) &amp;&amp; (SYSTEM_INFO.wProcessorArchitecture==PROCESSOR_ARCHITECTURE_AMD64)</td>
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
 

You should not  rely upon only the <b>VER_SUITE_SMALLBUSINESS</b> flag to determine 
    whether Small Business Server has been installed on the system, as both this flag and the 
    <b>VER_SUITE_SMALLBUSINESS_RESTRICTED</b> flag are set when this product suite is installed. If 
    you upgrade this installation to Windows Server, Standard Edition, the 
    <b>VER_SUITE_SMALLBUSINESS_RESTRICTED</b> flag will be cleared—however, the 
    <b>VER_SUITE_SMALLBUSINESS flag</b> will remain set. In this case, this indicates that Small 
    Business Server was once installed on this system. If this installation is further upgraded to Windows Server, 
    Enterprise Edition, the <b>VER_SUITE_SMALLBUSINESS</b> flag will remain set.

If compatibility mode is in effect, the <b>OSVERSIONINFOEX</b> structure contains information about the operating system that is selected for <a href="/previous-versions/bb757005(v=msdn.10)">application compatibility</a>.

To determine whether a Win32-based application is running on WOW64, call the 
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process">IsWow64Process</a> function. To determine whether the system is running a  64-bit version of Windows, call the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a> function.

The <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function provides the 
    following additional information about the current operating system. 

<table>
<tr>
<th>Product</th>
<th>Setting</th>
</tr>
<tr>
<td>Windows Server 2003 R2</td>
<td><b>SM_SERVERR2</b></td>
</tr>
<tr>
<td>Windows XP Media Center Edition</td>
<td><b>SM_MEDIACENTER</b></td>
</tr>
<tr>
<td>Windows XP Starter Edition</td>
<td><b>SM_STARTER</b></td>
</tr>
<tr>
<td>Windows XP Tablet PC Edition</td>
<td><b>SM_TABLETPC</b></td>
</tr>
</table>
 


#### Examples

For an example, see 
     <a href="/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.

<div class="code"></div>




> [!NOTE]
> The winnt.h header defines OSVERSIONINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process">IsWow64Process</a>



<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a>



<a href="/windows/desktop/SysInfo/version-helper-apis">Version Helper APIs</a>
