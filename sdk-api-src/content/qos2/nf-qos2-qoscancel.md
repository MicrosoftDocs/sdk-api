---
UID: NF:qos2.QOSCancel
title: QOSCancel function (qos2.h)
description: Cancels a pending overlapped operation, like QOSSetFlow.
helpviewer_keywords: ["QOSCancel","QOSCancel function [QOS]","qos.qoscancel","qos2/QOSCancel"]
old-location: qos\qoscancel.htm
tech.root: QOS
ms.assetid: d1f6f32f-d105-40cb-8113-319aa1f63c77
ms.date: 12/05/2018
ms.keywords: QOSCancel, QOSCancel function [QOS], qos.qoscancel, qos2/QOSCancel
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
 - QOSCancel
 - qos2/QOSCancel
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
 - QOSCancel
---

# QOSCancel function


## -description

The <b>QOSCancel</b> function cancels a pending overlapped operation, like  <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a>.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param Overlapped [in]

Pointer to the OVERLAPPED structure used in the operation to be canceled.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0.  To get extended error information, call <b>GetLastError</b>. Some possible error codes follow.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Overlapped</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failed.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ADAP_HDW_ERR</b></dt>
</dl>
</td>
<td width="60%">
A network adapter hardware error occurred.

</td>
</tr>
</table>

## -remarks

This function would never be called with a <b>NULL</b><i>Overlapped</i> parameter.

Successfully canceled operations complete normal completion mechanisms and return <b>ERROR_OPERATION_ABORTED</b> as their completion return code.

Closing a handle with the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosclosehandle">QOSCloseHandle</a> will automatically abort all pending operations issued with that handle.  If the handle is closed while a <b>QOSCancel</b> is still in progress, the call will complete with <b>ERROR_OPERATION_ABORTED</b> as the return code.

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>