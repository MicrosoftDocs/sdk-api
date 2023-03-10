---
UID: NS:lmwksta._WKSTA_INFO_101
title: WKSTA_INFO_101 (lmwksta.h)
description: Contains information about a workstation environment, including platform-specific information, the name of the domain and the local computer, and information concerning the operating system. (WKSTA_INFO_101)
helpviewer_keywords: ["*LPWKSTA_INFO_101","*PWKSTA_INFO_101","LPWKSTA_INFO_101","LPWKSTA_INFO_101 structure pointer [Network Management]","PLATFORM_ID_DOS","PLATFORM_ID_NT","PLATFORM_ID_OS2","PLATFORM_ID_OSF","PLATFORM_ID_VMS","PWKSTA_INFO_101","PWKSTA_INFO_101 structure pointer [Network Management]","WKSTA_INFO_101","WKSTA_INFO_101 structure [Network Management]","_win32_wksta_info_101_str","lmwksta/LPWKSTA_INFO_101","lmwksta/PWKSTA_INFO_101","lmwksta/WKSTA_INFO_101","netmgmt.wksta_info_101_str"]
old-location: netmgmt\wksta_info_101_str.htm
tech.root: NetMgmt
ms.assetid: 2b692d40-6229-45ef-9ec6-ee464bba0696
ms.date: 12/05/2018
ms.keywords: '*LPWKSTA_INFO_101, *PWKSTA_INFO_101, LPWKSTA_INFO_101, LPWKSTA_INFO_101 structure pointer [Network Management], PLATFORM_ID_DOS, PLATFORM_ID_NT, PLATFORM_ID_OS2, PLATFORM_ID_OSF, PLATFORM_ID_VMS, PWKSTA_INFO_101, PWKSTA_INFO_101 structure pointer [Network Management], WKSTA_INFO_101, WKSTA_INFO_101 structure [Network Management], _win32_wksta_info_101_str, lmwksta/LPWKSTA_INFO_101, lmwksta/PWKSTA_INFO_101, lmwksta/WKSTA_INFO_101, netmgmt.wksta_info_101_str'
req.header: lmwksta.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WKSTA_INFO_101, *PWKSTA_INFO_101, *LPWKSTA_INFO_101
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WKSTA_INFO_101
 - lmwksta/_WKSTA_INFO_101
 - PWKSTA_INFO_101
 - lmwksta/PWKSTA_INFO_101
 - WKSTA_INFO_101
 - lmwksta/WKSTA_INFO_101
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_INFO_101
---

# WKSTA_INFO_101 structure


## -description

The
				<b>WKSTA_INFO_101</b> structure contains information about a workstation environment, including platform-specific information, the name of the domain and the local computer, and information concerning the operating system.

## -struct-fields

### -field wki101_platform_id

Type: <b>DWORD</b>

The information level to use to retrieve platform-specific information. 

Possible values for this member are listed in the <i>Lmcons.h</i> header file.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_DOS"></a><a id="platform_id_dos"></a><dl>
<dt><b>PLATFORM_ID_DOS</b></dt>
<dt>300</dt>
</dl>
</td>
<td width="60%">
The MS-DOS platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_OS2"></a><a id="platform_id_os2"></a><dl>
<dt><b>PLATFORM_ID_OS2</b></dt>
<dt>400</dt>
</dl>
</td>
<td width="60%">
The OS/2 platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_NT"></a><a id="platform_id_nt"></a><dl>
<dt><b>PLATFORM_ID_NT</b></dt>
<dt>500</dt>
</dl>
</td>
<td width="60%">
The Windows NT platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_OSF"></a><a id="platform_id_osf"></a><dl>
<dt><b>PLATFORM_ID_OSF</b></dt>
<dt>600</dt>
</dl>
</td>
<td width="60%">
The OSF platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_VMS"></a><a id="platform_id_vms"></a><dl>
<dt><b>PLATFORM_ID_VMS</b></dt>
<dt>700</dt>
</dl>
</td>
<td width="60%">
The VMS platform.

</td>
</tr>
</table>

### -field wki101_computername

Type: <b>LMSTR</b>

A pointer to a string specifying the name of the local computer.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field wki101_langroup

Type: <b>LMSTR</b>

A pointer to a string specifying the name of the domain to which the computer belongs.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field wki101_ver_major

Type: <b>DWORD</b>

The major version number of the operating system running on the computer.

### -field wki101_ver_minor

Type: <b>DWORD</b>

The minor version number of the operating system running on the computer.

### -field wki101_lanroot

Type: <b>LMSTR</b>

A pointer to a string that contains the path to the LANMAN directory.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstagetinfo">NetWkstaGetInfo</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstasetinfo">NetWkstaSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>
