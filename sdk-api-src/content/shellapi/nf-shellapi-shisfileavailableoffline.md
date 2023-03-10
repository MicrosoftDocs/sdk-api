---
UID: NF:shellapi.SHIsFileAvailableOffline
title: SHIsFileAvailableOffline function (shellapi.h)
description: Determines whether a file or folder is available for offline use. This function also determines whether the file would be opened from the network, from the local Offline Files cache, or from both locations.
helpviewer_keywords: ["OFFLINE_STATUS_INCOMPLETE","OFFLINE_STATUS_LOCAL","OFFLINE_STATUS_REMOTE","SHIsFileAvailableOffline","SHIsFileAvailableOffline function [Windows Shell]","shell.SHIsFileAvailableOffline","shell_shisfileavailableoffline","shellapi/SHIsFileAvailableOffline"]
old-location: shell\SHIsFileAvailableOffline.htm
tech.root: shell
ms.assetid: 9acf212d-9309-42b0-ba96-faa0ecf0b865
ms.date: 12/05/2018
ms.keywords: OFFLINE_STATUS_INCOMPLETE, OFFLINE_STATUS_LOCAL, OFFLINE_STATUS_REMOTE, SHIsFileAvailableOffline, SHIsFileAvailableOffline function [Windows Shell], shell.SHIsFileAvailableOffline, shell_shisfileavailableoffline, shellapi/SHIsFileAvailableOffline
req.header: shellapi.h
req.include-header: 
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHIsFileAvailableOffline
 - shellapi/SHIsFileAvailableOffline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHIsFileAvailableOffline
---

# SHIsFileAvailableOffline function


## -description

Determines whether a file or folder is available for offline use. This function also determines whether the file would be opened from the network, from the local Offline Files cache, or from both locations.

## -parameters

### -param pwszPath [in]

Type: <b>PCWSTR</b>

A pointer to a string value that specifies the full path to a network file or directory. This path does not need to be in UNC form. If <i>pszPath</i> is not a network path, the function returns E_INVALIDARG.

### -param pdwStatus [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable of type <b>DWORD</b> that receives one or more of the following flags if the function succeeds.



#### OFFLINE_STATUS_LOCAL (0x01)

If the file is open, it is open in the cache.



#### OFFLINE_STATUS_REMOTE (0x02)

If the file is open, it is open on the server.



#### OFFLINE_STATUS_INCOMPLETE (0x04)

The local copy is currently incomplete. The file cannot be opened in offline mode until it has been synchronized.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The file or directory is cached.  It is available offline unless <b>OFFLINE_STATUS_INCOMPLETE</b> is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The path is invalid or not a network path. The file or directory is not cached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The file or directory is not cached.

</td>
</tr>
</table>

## -remarks

If <i>pszPath</i> is a directory, <b>SHIsFileAvailableOffline</b> will not return the <b>OFFLINE_STATUS_INCOMPLETE</b> flag.

If <b>SHIsFileAvailableOffline</b> returns both <b>OFFLINE_STATUS_LOCAL</b> and <b>OFFLINE_STATUS_REMOTE</b>, the file or directory is open in both places.  This is common when the server is online.

