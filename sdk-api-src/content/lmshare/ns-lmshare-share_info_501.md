---
UID: NS:lmshare._SHARE_INFO_501
title: SHARE_INFO_501 (lmshare.h)
author: windows-sdk-content
description: Contains information about the shared resource including the name and type of the resource, and a comment associated with the resource.
old-location: fs\share_info_501_str.htm
tech.root: NetShare
ms.assetid: 2900d84c-7357-4652-b8b3-c9734fcc0449
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSHARE_INFO_501, *PSHARE_INFO_501, LPSHARE_INFO_501, LPSHARE_INFO_501 structure pointer [Files], PSHARE_INFO_501, PSHARE_INFO_501 structure pointer [Files], SHARE_INFO_501, SHARE_INFO_501 structure [Files], STYPE_DEVICE, STYPE_DISKTREE, STYPE_IPC, STYPE_PRINTQ, STYPE_SPECIAL, STYPE_TEMPORARY, _win32_share_info_501_str, fs.share_info_501_str, lmshare/LPSHARE_INFO_501, lmshare/PSHARE_INFO_501, lmshare/SHARE_INFO_501, netmgmt.share_info_501_str"
ms.topic: struct
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Lmshare.h
api_name:
 - SHARE_INFO_501
product: Windows
targetos: Windows
req.typenames: SHARE_INFO_501, *PSHARE_INFO_501, *LPSHARE_INFO_501
req.redist: 
---

# SHARE_INFO_501 structure


## -description


Contains information about the shared resource including the name and type of the resource, and a comment associated with the resource.


## -struct-fields




### -field shi501_netname

Pointer to a Unicode string specifying the name of a shared resource.


### -field shi501_type

A combination of values that specify the type of share. 



One of the following values may be specified. You can isolate these values by using the <b>STYPE_MASK</b> value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_DISKTREE"></a><a id="stype_disktree"></a><dl>
<dt><b>STYPE_DISKTREE</b></dt>
</dl>
</td>
<td width="60%">
Disk drive.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_PRINTQ"></a><a id="stype_printq"></a><dl>
<dt><b>STYPE_PRINTQ</b></dt>
</dl>
</td>
<td width="60%">
Print queue.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_DEVICE"></a><a id="stype_device"></a><dl>
<dt><b>STYPE_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
Communication device.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_IPC"></a><a id="stype_ipc"></a><dl>
<dt><b>STYPE_IPC</b></dt>
</dl>
</td>
<td width="60%">
Interprocess communication (IPC).

</td>
</tr>
</table>
 

In addition, one or both of the following values may be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_SPECIAL"></a><a id="stype_special"></a><dl>
<dt><b>STYPE_SPECIAL</b></dt>
</dl>
</td>
<td width="60%">
Special share reserved for interprocess communication (IPC$) or remote administration of the server (ADMIN$). Can also refer to administrative shares such as C$, D$, E$, and so forth. For more information, see <a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_TEMPORARY"></a><a id="stype_temporary"></a><dl>
<dt><b>STYPE_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
A temporary share.

</td>
</tr>
</table>
 


### -field shi501_remark

Pointer to a Unicode string specifying an optional comment about the shared resource.


### -field shi501_flags

Reserved; must be zero.


## -see-also




<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

