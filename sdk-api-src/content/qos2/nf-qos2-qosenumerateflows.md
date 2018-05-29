---
UID: NF:qos2.QOSEnumerateFlows
title: QOSEnumerateFlows function
author: windows-sdk-content
description: Enumerates all existing flows.
old-location: qos\qosenumerateflows.htm
old-project: QOS
ms.assetid: 62027f7b-9ecc-4631-b755-2302e0bb49c0
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: QOSEnumerateFlows, QOSEnumerateFlows function [QOS], qos.qosenumerateflows, qos2/QOSEnumerateFlows
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: QOS_TRAFFIC_TYPE, *PQOS_TRAFFIC_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	qwave.dll
api_name:
-	QOSEnumerateFlows
product: Windows
targetos: Windows
req.lib: Qwave.lib
req.dll: Qwave.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# QOSEnumerateFlows function


## -description


The <b>QOSEnumerateFlows</b> function enumerates all existing flows.


## -parameters




### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a>.


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
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a> again.

</td>
</tr>
</table>
 




## -remarks



Successfully calling this function requires administrative privileges

Calling the <b>QOSEnumerateFlows</b> function retrieves a list of <b>QOS_FlowId</b>s currently active on the QOS subsystem.   These <b>QOS_FlowId</b>s could then be used to call the <a href="https://msdn.microsoft.com/8cae3ba2-beca-45e2-9526-2d917abc2606">QOSQueryFlow</a> function in order to gain more information on individual flows.

This function has call-twice semantics. First call to get the <i>Buffer</i> size, then call again (with an appropriately sized <i>Buffer</i> if the first call failed with <b>ERROR_INSUFFICIENT_BUFFER</b>) to retrieve the list of flows.  The second call may fail again with <b>ERROR_INSUFFICIENT_BUFFER</b> if new flows ere added since the first call.

Flows from another process cannot be modified.




## -see-also




<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

