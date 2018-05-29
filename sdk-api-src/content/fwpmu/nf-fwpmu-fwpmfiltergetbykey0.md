---
UID: NF:fwpmu.FwpmFilterGetByKey0
title: FwpmFilterGetByKey0 function
author: windows-sdk-content
description: Retrieves a filter object.
old-location: fwp\fwpmfiltergetbykey0_func.htm
old-project: FWP
ms.assetid: 5ab0942c-aee2-44f9-9e7f-568405131691
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmFilterGetByKey0, FwpmFilterGetByKey0 function [Filtering], fwp.fwpmfiltergetbykey0_func, fwpmu/FwpmFilterGetByKey0
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmFilterGetByKey0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmFilterGetByKey0 function


## -description


The <b>FwpmFilterGetByKey0</b> function retrieves a filter object.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the filter. This GUID was specified in the <b>filterKey</b> member of the <i>filter</i> parameter when the application called <a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a> for this object.


### -param filter [out]

Type: <b><a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a>**</b>

The filter information.


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
The filter was retrieved successfully.

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

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the filter. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmFilterGetByKey0</b> is a specific implementation of FwpmFilterGetByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a>



<a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a>



<a href="https://msdn.microsoft.com/75c0796c-84d0-4282-bc93-267a17dd3edc">FwpmFilterDeleteByKey0</a>
 

 

