---
UID: NF:ntmsapi.GetNtmsMediaPoolNameA
title: GetNtmsMediaPoolNameA function (ntmsapi.h)
description: The GetNtmsMediaPoolName function retrieves the specified media pool's full name hierarchy. (ANSI)
helpviewer_keywords: ["GetNtmsMediaPoolNameA", "ntmsapi/GetNtmsMediaPoolNameA"]
old-location: fs\getntmsmediapoolname.htm
tech.root: fs
ms.assetid: 72b9028b-d97e-4441-8677-1a4a0b03dee2
ms.date: 12/05/2018
ms.keywords: GetNtmsMediaPoolName, GetNtmsMediaPoolName function [Files], GetNtmsMediaPoolNameA, GetNtmsMediaPoolNameW, _zaw_getntmsmediapoolname, base.getntmsmediapoolname, fs.getntmsmediapoolname, ntmsapi/GetNtmsMediaPoolName, ntmsapi/GetNtmsMediaPoolNameA, ntmsapi/GetNtmsMediaPoolNameW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNtmsMediaPoolNameW (Unicode) and GetNtmsMediaPoolNameA (ANSI)
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
 - GetNtmsMediaPoolNameA
 - ntmsapi/GetNtmsMediaPoolNameA
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
 - GetNtmsMediaPoolName
 - GetNtmsMediaPoolNameA
 - GetNtmsMediaPoolNameW
---

# GetNtmsMediaPoolNameA function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetNtmsMediaPoolName</b> function retrieves the specified media pool's full name hierarchy.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpPoolId [in]

Unique identifier of the media pool whose name is to be retrieved.

### -param lpNameBuf [out]

Pointer to a buffer that receives the name of the media pool.

### -param lpdwBufSize [in, out]

Size of the <i>lpBufName</i> buffer, on input. On output, the number of characters in the full name hierarchy.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size is not large enough. The correct size is returned in <i>lpdwBufSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA_POOL</b></dt>
</dl>
</td>
<td width="60%">
The media pool ID is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The memory allocation failed.

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
</table>

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-createntmsmediapool">CreateNtmsMediaPool</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>

## -remarks

> [!NOTE]
> The ntmsapi.h header defines GetNtmsMediaPoolName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
