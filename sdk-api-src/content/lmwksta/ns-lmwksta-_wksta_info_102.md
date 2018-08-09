---
UID: NS:lmwksta._WKSTA_INFO_102
title: "_WKSTA_INFO_102"
author: windows-sdk-content
description: Contains information about a workstation environment, including platform-specific information, the name of the domain and the local computer, and information concerning the operating system.
old-location: netmgmt\wksta_info_102_str.htm
old-project: netmgmt
ms.assetid: 01607fb5-c433-439c-aaaa-3736697f7c07
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPWKSTA_INFO_102, *PWKSTA_INFO_102, LPWKSTA_INFO_102, LPWKSTA_INFO_102 structure pointer [Network Management], PLATFORM_ID_DOS, PLATFORM_ID_NT, PLATFORM_ID_OS2, PLATFORM_ID_OSF, PLATFORM_ID_VMS, PWKSTA_INFO_102, PWKSTA_INFO_102 structure pointer [Network Management], WKSTA_INFO_102, WKSTA_INFO_102 structure [Network Management], _WKSTA_INFO_102, _win32_wksta_info_102_str, lmwksta/LPWKSTA_INFO_102, lmwksta/PWKSTA_INFO_102, lmwksta/WKSTA_INFO_102, netmgmt.wksta_info_102_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WKSTA_INFO_102, *PWKSTA_INFO_102, *LPWKSTA_INFO_102
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_INFO_102
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _WKSTA_INFO_102 structure


## -description


The
				<b>WKSTA_INFO_102</b> structure contains information about a workstation environment, including platform-specific information, the name of the domain and the local computer, and information concerning the operating system.


## -struct-fields




### -field wki102_platform_id

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
 


### -field wki102_computername

Type: <b>LMSTR</b>

A pointer to a string specifying the name of the local computer.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field wki102_langroup

Type: <b>LMSTR</b>

A pointer to a string specifying the name of the domain to which the computer belongs.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field wki102_ver_major

Type: <b>DWORD</b>

The major version number of the operating system running on the computer.


### -field wki102_ver_minor

Type: <b>DWORD</b>

The minor version number of the operating system running on the computer.


### -field wki102_lanroot

Type: <b>LMSTR</b>

A pointer to a string that contains the path to the LANMAN directory.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field wki102_logged_on_users

Type: <b>DWORD</b>

The number of users who are logged on to the local computer.


## -see-also




<a href="https://msdn.microsoft.com/08777069-1afd-4482-8090-c65ef0bec1ea">NetWkstaGetInfo</a>



<a href="https://msdn.microsoft.com/d746b6c9-5ef1-4174-a84f-44e4e50200cd">NetWkstaSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/cc400f43-297b-4ff4-8353-b268839c48b8">Workstation and Workstation User Functions</a>
 

 

