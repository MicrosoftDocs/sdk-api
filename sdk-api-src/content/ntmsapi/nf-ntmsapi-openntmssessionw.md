---
UID: NF:ntmsapi.OpenNtmsSessionW
title: OpenNtmsSessionW function (ntmsapi.h)
description: The OpenNtmsSession function sets up a session with a RSM server. (Unicode)
helpviewer_keywords: ["OpenNtmsSession", "OpenNtmsSession function [Files]", "OpenNtmsSessionW", "_zaw_openntmssession", "base.openntmssession", "fs.openntmssession", "ntmsapi/OpenNtmsSession", "ntmsapi/OpenNtmsSessionW"]
old-location: fs\openntmssession.htm
tech.root: fs
ms.assetid: 5a323911-e99c-4f81-9580-0feac2f0a54e
ms.date: 12/05/2018
ms.keywords: OpenNtmsSession, OpenNtmsSession function [Files], OpenNtmsSessionA, OpenNtmsSessionW, _zaw_openntmssession, base.openntmssession, fs.openntmssession, ntmsapi/OpenNtmsSession, ntmsapi/OpenNtmsSessionA, ntmsapi/OpenNtmsSessionW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenNtmsSessionW (Unicode) and OpenNtmsSessionA (ANSI)
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
 - OpenNtmsSessionW
 - ntmsapi/OpenNtmsSessionW
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
 - OpenNtmsSession
 - OpenNtmsSessionA
 - OpenNtmsSessionW
---

# OpenNtmsSessionW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>OpenNtmsSession</b> function sets up a session with a RSM server.

## -parameters

### -param lpServer [in]

RSM server name. If this parameter is <b>NULL</b>, the current computer name is used.

### -param lpApplication [in]

Unique character string that identifies the application. This name identifies resources and operator requests. This parameter is optional and may be <b>NULL</b>.

### -param dwOptions

Reserved; must be zero.

## -returns

If 
<b>OpenNtmsSession</b> succeeds, it returns a handle that uniquely identifies this session. If the function fails, it returns INVALID_HANDLE_VALUE. To retrieve more information, call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. This function can return one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_COMPUTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The computer name format that was specified was not in a valid format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not started or not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
RSM service has not started. The application should wait and retry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALID_HANDLE_VALUE</b></dt>
</dl>
</td>
<td width="60%">
RSM cannot open a session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_INTERFACES</b></dt>
</dl>
</td>
<td width="60%">
The service is using an older version of RSM than your application.

</td>
</tr>
</table>

## -remarks

The 
<b>OpenNtmsSession</b> function returns a session handle used with other RSM functions, establishes a connection with the RSM database, and initializes the RSM subsystem for the application.

When 
<b>OpenNtmsSession</b> returns, the application can perform RSM operations.

Sessions are thread-safe but cannot be passed among processes.





> [!NOTE]
> The ntmsapi.h header defines OpenNtmsSession as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-closentmssession">CloseNtmsSession</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Session Management Functions</a>
