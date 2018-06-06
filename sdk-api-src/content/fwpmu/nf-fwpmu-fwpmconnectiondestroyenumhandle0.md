---
UID: NF:fwpmu.FwpmConnectionDestroyEnumHandle0
title: FwpmConnectionDestroyEnumHandle0 function
author: windows-sdk-content
description: Frees a handle returned by FwpmConnectionCreateEnumHandle0.
old-location: fwp\fwpmconnectiondestroyenumhandle0.htm
old-project: FWP
ms.assetid: 0325908e-4d2b-4cdb-9cfa-f2985a76dba9
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmConnectionDestroyEnumHandle0, FwpmConnectionDestroyEnumHandle0 function [Filtering], fwp.fwpmconnectiondestroyenumhandle0, fwpmu/FwpmConnectionDestroyEnumHandle0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FwpmConnectionDestroyEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmConnectionDestroyEnumHandle0 function


## -description


The <b>FwpmConnectionDestroyEnumHandle0</b> function frees a handle returned by <a href="https://msdn.microsoft.com/b33878d5-437d-4625-b488-28fbe95eb69f">FwpmConnectionCreateEnumHandle0</a>.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a connection object enumeration created by a call to <a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/b33878d5-437d-4625-b488-28fbe95eb69f">FwpmConnectionCreateEnumHandle0</a>



<a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>
 

 

