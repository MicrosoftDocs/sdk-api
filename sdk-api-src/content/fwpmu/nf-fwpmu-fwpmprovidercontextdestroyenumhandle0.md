---
UID: NF:fwpmu.FwpmProviderContextDestroyEnumHandle0
title: FwpmProviderContextDestroyEnumHandle0 function
author: windows-sdk-content
description: Frees a handle returned by FwpmProviderContextCreateEnumHandle0.
old-location: fwp\fwpmprovidercontextdestroyenumhandle0_func.htm
old-project: FWP
ms.assetid: 85ec36f8-c6e0-4dcf-aad2-15d61aa6bd64
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmProviderContextDestroyEnumHandle0, FwpmProviderContextDestroyEnumHandle0 function [Filtering], fwp.fwpmprovidercontextdestroyenumhandle0_func, fwpmu/FwpmProviderContextDestroyEnumHandle0
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
 - FwpmProviderContextDestroyEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmProviderContextDestroyEnumHandle0 function


## -description


The <b>FwpmProviderContextDestroyEnumHandle0</b> function frees a handle returned by <a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a provider context enumeration created by a call to <a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>.


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
The enumerator was successfully deleted.

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



<b>FwpmProviderContextDestroyEnumHandle0</b> is a specific implementation of FwpmProviderContextDestroyEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>
 

 

