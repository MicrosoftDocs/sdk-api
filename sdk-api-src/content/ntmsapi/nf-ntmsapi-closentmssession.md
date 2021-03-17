---
UID: NF:ntmsapi.CloseNtmsSession
title: CloseNtmsSession function (ntmsapi.h)
description: The CloseNtmsSession function closes the specified RSM session.
helpviewer_keywords: ["CloseNtmsSession","CloseNtmsSession function [Files]","_zaw_closentmssession","base.closentmssession","fs.closentmssession","ntmsapi/CloseNtmsSession"]
old-location: fs\closentmssession.htm
tech.root: fs
ms.assetid: 54bc354a-fdef-4642-8e53-cf20ed374000
ms.date: 12/05/2018
ms.keywords: CloseNtmsSession, CloseNtmsSession function [Files], _zaw_closentmssession, base.closentmssession, fs.closentmssession, ntmsapi/CloseNtmsSession
req.header: ntmsapi.h
req.include-header: 
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CloseNtmsSession
 - ntmsapi/CloseNtmsSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - CloseNtmsSession
---

# CloseNtmsSession function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CloseNtmsSession</b> function closes the specified RSM session.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CONNECTION_UNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
Connection to the RSM server or domain is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not a valid session handle.

</td>
</tr>
</table>

## -remarks

The 
<b>CloseNtmsSession</b> function releases all resources. Use of a closed session handle returns an error code.

If a call to the 
<b>CloseNtmsSession</b> function occurs while an application has an outstanding synchronous request (for example, a mount or dismount request), the request is unwound and canceled.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Session Management Functions</a>