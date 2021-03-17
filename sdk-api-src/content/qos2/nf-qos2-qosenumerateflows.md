---
UID: NF:qos2.QOSEnumerateFlows
title: QOSEnumerateFlows function (qos2.h)
description: Enumerates all existing flows.
helpviewer_keywords: ["QOSEnumerateFlows","QOSEnumerateFlows function [QOS]","qos.qosenumerateflows","qos2/QOSEnumerateFlows"]
old-location: qos\qosenumerateflows.htm
tech.root: QOS
ms.assetid: 62027f7b-9ecc-4631-b755-2302e0bb49c0
ms.date: 12/05/2018
ms.keywords: QOSEnumerateFlows, QOSEnumerateFlows function [QOS], qos.qosenumerateflows, qos2/QOSEnumerateFlows
req.header: qos2.h
req.include-header: Qos2.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Qwave.lib
req.dll: Qwave.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QOSEnumerateFlows
 - qos2/QOSEnumerateFlows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - qwave.dll
api_name:
 - QOSEnumerateFlows
---

# QOSEnumerateFlows function


## -description

The <b>QOSEnumerateFlows</b> function enumerates all existing flows.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param Size [in, out]

Indicates the size of the <i>Buffer</i> parameter, in bytes.

On function return, if successful, this parameter will specify the number of bytes copied into <i>Buffer</i>.

If this call fails with <b>ERROR_INSUFFICIENT_BUFFER</b>, this parameter will indicate the minimum required <i>Buffer</i> size in order to successfully complete this operation.

### -param Buffer [out]

Pointer to an array of <b>QOS_FlowId</b> flow identifiers. A <b>QOS_FlowId</b> is an unsigned 32-bit integer.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0.  To get extended error information, call <b>GetLastError</b>.  Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>QOSHandle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Buffer is too small.  On output, <i>Size</i> will contain the minimum required buffer size. This function should then be called again with a buffer of the indicated size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>DestAddr</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are insufficient resources to carry out the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The request could not be performed because of an I/O device error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_REINITIALIZATION_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> again.

</td>
</tr>
</table>

## -remarks

Successfully calling this function requires administrative privileges

Calling the <b>QOSEnumerateFlows</b> function retrieves a list of <b>QOS_FlowId</b>s currently active on the QOS subsystem.   These <b>QOS_FlowId</b>s could then be used to call the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a> function in order to gain more information on individual flows.

This function has call-twice semantics. First call to get the <i>Buffer</i> size, then call again (with an appropriately sized <i>Buffer</i> if the first call failed with <b>ERROR_INSUFFICIENT_BUFFER</b>) to retrieve the list of flows.  The second call may fail again with <b>ERROR_INSUFFICIENT_BUFFER</b> if new flows ere added since the first call.

Flows from another process cannot be modified.

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>