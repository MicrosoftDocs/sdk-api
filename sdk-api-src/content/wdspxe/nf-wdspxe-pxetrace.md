---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PxeTrace function


## -description


Adds a trace entry to the PXE log.


## -parameters




### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> function.


### -param Severity [in]

Severity of trace entry.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_VERBOSE"></a><a id="pxe_trace_verbose"></a><dl>
<dt><b>PXE_TRACE_VERBOSE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The trace entry is verbose and would primarily be useful when debugging.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_INFO"></a><a id="pxe_trace_info"></a><dl>
<dt><b>PXE_TRACE_INFO</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The trace entry is informational, but does not indicate a warning condition.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_WARNING"></a><a id="pxe_trace_warning"></a><dl>
<dt><b>PXE_TRACE_WARNING</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The trace message indicates a warning.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_ERROR"></a><a id="pxe_trace_error"></a><dl>
<dt><b>PXE_TRACE_ERROR</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The trace message indicates an error condition.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_FATAL"></a><a id="pxe_trace_fatal"></a><dl>
<dt><b>PXE_TRACE_FATAL</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The trace message indicates a fatal error condition.

</td>
</tr>
</table>
 


### -param pszFormat [in]

Address of a buffer that contains a printf-style format string.


### -param param

TBD




####### - ...

Optional arguments. The number and type of argument parameters depend on the format control string pointed 
      to by the <i>pszFormat</i> parameter.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

