---
UID: NS:lmserver._SERVER_INFO_100
title: "_SERVER_INFO_100"
author: windows-sdk-content
description: The SERVER_INFO_100 structure contains information about the specified server, including the name and platform.
old-location: netmgmt\server_info_100_str.htm
tech.root: NetMgmt
ms.assetid: b027a669-b4d8-4d42-aedc-94834bf099da
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSERVER_INFO_100, *PSERVER_INFO_100, LPSERVER_INFO_100, LPSERVER_INFO_100 structure pointer [Network Management], PLATFORM_ID_DOS, PLATFORM_ID_NT, PLATFORM_ID_OS2, PLATFORM_ID_OSF, PLATFORM_ID_VMS, PSERVER_INFO_100, PSERVER_INFO_100 structure pointer [Network Management], SERVER_INFO_100, SERVER_INFO_100 structure [Network Management], _SERVER_INFO_100, _win32_server_info_100_str, lmserver/LPSERVER_INFO_100, lmserver/PSERVER_INFO_100, lmserver/SERVER_INFO_100, netmgmt.server_info_100_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmserver.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_100
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_100, *PSERVER_INFO_100, *LPSERVER_INFO_100
req.redist: 
---

# _SERVER_INFO_100 structure


## -description


The
				<b>SERVER_INFO_100</b> structure contains information about the specified server, including the name and platform.


## -struct-fields




### -field sv100_platform_id

Type: <b>DWORD</b>

The information level to use for platform-specific information.

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
 


### -field sv100_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of the server.


## -see-also




<a href="https://msdn.microsoft.com/56c981f4-7a1d-4465-bd7b-5996222c4210">NetServerDiskEnum</a>



<a href="https://msdn.microsoft.com/10012a87-805e-4817-9f09-9e5632b1fa09">NetServerEnum</a>



<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

