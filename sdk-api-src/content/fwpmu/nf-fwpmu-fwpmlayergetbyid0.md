---
UID: NF:fwpmu.FwpmLayerGetById0
title: FwpmLayerGetById0 function
author: windows-sdk-content
description: Retrieves a layer object.
old-location: fwp\fwpmlayergetbyid0_func.htm
tech.root: fwp
ms.assetid: c7668d06-8533-4dd1-a4f6-fb38c97219db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FwpmLayerGetById0, FwpmLayerGetById0 function [Filtering], fwp.fwpmlayergetbyid0_func, fwpmu/FwpmLayerGetById0
ms.topic: function
req.header: fwpmu.h
req.include-header: 
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmLayerGetById0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmLayerGetById0 function


## -description


The <b>FwpmLayerGetById0</b> function retrieves a layer object.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT16</b>

 Identifier of the desired layer. For a list of possible values, see <a href="http://go.microsoft.com/fwlink/p/?linkid=229388">Run-time Filtering Layer Identifiers</a>  in the WDK documentation for Windows Filtering Platform.


### -param layer [out]

Type: <b><a href="https://msdn.microsoft.com/77d567a7-9495-4f16-9b02-e44a1ef67022">FWPM_LAYER0</a>**</b>

The layer information.


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
The layer was retrieved successfully.

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

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the layer. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmLayerGetById0</b> is a specific implementation of FwpmLayerGetById. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/77d567a7-9495-4f16-9b02-e44a1ef67022">FWPM_LAYER0</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=229388">Run-time Filtering Layer Identifiers</a>
 

 

