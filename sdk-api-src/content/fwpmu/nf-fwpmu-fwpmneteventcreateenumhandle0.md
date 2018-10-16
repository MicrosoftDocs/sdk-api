---
UID: NF:fwpmu.FwpmNetEventCreateEnumHandle0
title: FwpmNetEventCreateEnumHandle0 function
author: windows-sdk-content
description: Creates a handle used to enumerate a set of network events.
old-location: fwp\fwpmneteventcreateenumhandle0.htm
tech.root: fwp
ms.assetid: 82e0f189-f283-43b2-b9d4-29e754c5c95e
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FwpmNetEventCreateEnumHandle0, FwpmNetEventCreateEnumHandle0 function [Filtering], fwp.fwpmneteventcreateenumhandle0, fwpmu/FwpmNetEventCreateEnumHandle0
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FwpmNetEventCreateEnumHandle0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmNetEventCreateEnumHandle0 function


## -description


The <b>FwpmNetEventCreateEnumHandle0</b> function creates a handle used to enumerate a set of network events.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/79711b24-e092-4a36-810a-6acad279eb90">FWPM_NET_EVENT_ENUM_TEMPLATE0</a>*</b>

  Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

The handle for network event enumeration.


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
The enumerator was created successfully.

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



If <i>enumTemplate</i> is <b>NULL</b>, all network event objects are returned.

The caller must call <a href="https://msdn.microsoft.com/c9a0b31b-28f2-4f55-8a08-5fea182f8954">FwpmNetEventDestroyEnumHandle0</a> to free the returned handle.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the events' containers. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmNetEventCreateEnumHandle0</b> is a specific implementation of FwpmNetEventCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/79711b24-e092-4a36-810a-6acad279eb90">FWPM_NET_EVENT_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/c9a0b31b-28f2-4f55-8a08-5fea182f8954">FwpmNetEventDestroyEnumHandle0</a>
 

 

