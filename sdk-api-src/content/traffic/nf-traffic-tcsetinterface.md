---
UID: NF:traffic.TcSetInterface
title: TcSetInterface function
author: windows-sdk-content
description: The TcSetInterface function sets individual parameters for a given interface.
old-location: qos\tcsetinterface.htm
old-project: qos
ms.assetid: 7ca28fac-999c-4386-81e7-65003e89d9c5
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: TcSetInterface, TcSetInterface function [QOS], _gqos_tcsetinterface, qos.tcsetinterface, traffic/TcSetInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: traffic.h
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Traffic.dll
api_name:
 - TcSetInterface
product: Windows
targetos: Windows
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TcSetInterface function


## -description


The 
<b>TcSetInterface</b> function sets individual parameters for a given interface.


## -parameters




### -param IfcHandle [in]

Handle associated with the interface to be set. This handle is obtained by a previous call to the 
<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a> function.


### -param pGuidParam [in]

Pointer to the globally unique identifier (GUID) that corresponds to the parameter to be set. A list of available GUIDs can be found in 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>.


### -param BufferSize [in]

Size of the client-provided buffer, in bytes.


### -param Buffer [in]

Pointer to a client-provided buffer. <i>Buffer</i> must contain the value to which the traffic control parameter provided in <i>pGuidParam</i> should be set.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Setting the GUID for the provided interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_INSTANCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The GUID is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_GUID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The device did not register for this GUID.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Use of the 
<b>TcSetInterface</b> function requires administrative privilege. The list of GUIDs that can be set is explained in 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>



<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a>
 

 

