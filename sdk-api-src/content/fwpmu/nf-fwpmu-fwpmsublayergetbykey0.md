---
UID: NF:fwpmu.FwpmSubLayerGetByKey0
title: FwpmSubLayerGetByKey0 function
author: windows-sdk-content
description: Retrieves a sublayer by its key.
old-location: fwp\fwpmsublayergetbykey0_func.htm
old-project: fwp
ms.assetid: 3435b4fb-abea-43cc-b1a9-a8bea673d72e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FwpmSubLayerGetByKey0, FwpmSubLayerGetByKey0 function [Filtering], fwp.fwpmsublayergetbykey0_func, fwpmu/FwpmSubLayerGetByKey0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmSubLayerGetByKey0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmSubLayerGetByKey0 function


## -description


The <b>FwpmSubLayerGetByKey0</b> function retrieves a sublayer by its key.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of  the sublayer. This is the same GUID that was specified when the application called <a href="https://msdn.microsoft.com/85a6f4a9-297f-491d-b2f7-38de21dbe06c">FwpmSubLayerAdd0</a>.


### -param subLayer [out]

Type: <b><a href="https://msdn.microsoft.com/ce689b1d-1f5c-4dde-96cd-9001de3827aa">FWPM_SUBLAYER0</a>**</b>

The sublayer information.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The sublayer was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



The caller must free the returned object by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the sublayer. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmSubLayerGetByKey0</b> is a specific implementation of FwpmSubLayerGetByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/ce689b1d-1f5c-4dde-96cd-9001de3827aa">FWPM_SUBLAYER0</a>



<a href="https://msdn.microsoft.com/85a6f4a9-297f-491d-b2f7-38de21dbe06c">FwpmSubLayerAdd0</a>
 

 

