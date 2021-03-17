---
UID: NS:xaudio2.XAUDIO2_DEBUG_CONFIGURATION
title: XAUDIO2_DEBUG_CONFIGURATION (xaudio2.h)
description: Contains the new global debug configuration for XAudio2. Used with the SetDebugConfiguration function.
helpviewer_keywords: ["XAUDIO2_DEBUG_CONFIGURATION","XAUDIO2_DEBUG_CONFIGURATION structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_debug_configuration","xaudio2/XAUDIO2_DEBUG_CONFIGURATION"]
old-location: xaudio2\xaudio2_debug_configuration.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_DEBUG_CONFIGURATION
ms.date: 12/05/2018
ms.keywords: XAUDIO2_DEBUG_CONFIGURATION, XAUDIO2_DEBUG_CONFIGURATION structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_debug_configuration, xaudio2/XAUDIO2_DEBUG_CONFIGURATION
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: XAUDIO2_DEBUG_CONFIGURATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_DEBUG_CONFIGURATION
 - xaudio2/XAUDIO2_DEBUG_CONFIGURATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_DEBUG_CONFIGURATION
---

# XAUDIO2_DEBUG_CONFIGURATION structure


## -description

Contains the new global debug configuration for XAudio2. Used with the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration">SetDebugConfiguration</a> function.

## -struct-fields

### -field TraceMask

Bitmask of enabled debug message types. Can be 0 or one or more of the following:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XAUDIO2_LOG_ERRORS</td>
<td>Log error messages. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_WARNINGS</td>
<td>Log warning messages. 
		   <div class="alert"><b>Note</b>  Enabling XAUDIO2_LOG_WARNINGS also enables XAUDIO2_LOG_ERRORS.</div>
<div> </div>
</td>
</tr>
<tr>
<td>XAUDIO2_LOG_INFO</td>
<td>Log informational messages. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_DETAIL</td>
<td>Log detailed informational messages.  
         <div class="alert"><b>Note</b>  Enabling XAUDIO2_LOG_DETAIL also enables XAUDIO2_LOG_INFO.</div>
<div> </div>
</td>
</tr>
<tr>
<td>XAUDIO2_LOG_API_CALLS</td>
<td>Log public API function entries and exits. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_FUNC_CALLS</td>
<td>Log internal function entries and exits. 
		   <div class="alert"><b>Note</b>  Enabling XAUDIO2_LOG_FUNC_CALLS also enables XAUDIO2_LOG_API_CALLS.</div>
<div> </div>
</td>
</tr>
<tr>
<td>XAUDIO2_LOG_TIMING</td>
<td>Log delays detected and other timing data. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_LOCKS</td>
<td>Log usage of critical sections and mutexes. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_MEMORY</td>
<td>Log memory heap usage information. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_STREAMING</td>
<td>Log audio streaming information. </td>
</tr>
</table>

### -field BreakMask

Message types that will cause an immediate break. Can be 0 or one of the following:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XAUDIO2_LOG_ERRORS</td>
<td>Break on error messages. </td>
</tr>
<tr>
<td>XAUDIO2_LOG_WARNINGS</td>
<td>Break on warning messages. 
                <div class="alert"><b>Note</b>  Enabling XAUDIO2_LOG_WARNINGS also enables XAUDIO2_LOG_ERRORS.</div>
<div> </div>
</td>
</tr>
</table>

### -field LogThreadID

Indicates whether to log the thread ID with each message.

### -field LogFileline

Indicates whether to log source files and line numbers.

### -field LogFunctionName

Indicates whether to log function names.

### -field LogTiming

Indicates whether to log message timestamps.

## -remarks

Debugging messages can be completely turned off by initializing <b>XAUDIO2_DEBUG_CONFIGURATION</b> to all zeroes.

<div class="alert"><b>Note</b>  For this version of XAudio2, only the <b>XAUDIO2_LOG_ERRORS</b> value is supported on <b>TraceMask</b> or <b>BreakMask</b>. All other members and values are ignored.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>