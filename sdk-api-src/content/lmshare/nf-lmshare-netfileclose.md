---
UID: NF:lmshare.NetFileClose
title: NetFileClose function (lmshare.h)
description: Forces a resource to close. This function can be used when an error prevents closure by any other means. You should use NetFileClose with caution because it does not write data cached on the client system to the file before closing the file.
helpviewer_keywords: ["NetFileClose","NetFileClose function [Files]","_win32_netfileclose","fs.netfileclose","lmshare/NetFileClose","netmgmt.netfileclose"]
old-location: fs\netfileclose.htm
tech.root: fs
ms.assetid: 36a5f464-fec3-4b4f-91c3-447ff5ff70af
ms.date: 12/05/2018
ms.keywords: NetFileClose, NetFileClose function [Files], _win32_netfileclose, fs.netfileclose, lmshare/NetFileClose, netmgmt.netfileclose
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetFileClose
 - lmshare/NetFileClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetFileClose
---

# NetFileClose function


## -description

Forces a resource to close. This function can be used when an error prevents closure by any other means. You should use 
<b>NetFileClose</b> with caution because it does not write data cached on the client system to the file before closing the file.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.

### -param fileid [in]

Specifies the file identifier of the opened resource instance to close.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file was not found.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetFileClose</b> function.

## -see-also

<a href="/windows/desktop/NetShare/netfile-functions">NetFile
		  Functions</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>