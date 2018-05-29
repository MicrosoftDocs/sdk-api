---
UID: NF:fwpmu.FwpmSessionCreateEnumHandle0
title: FwpmSessionCreateEnumHandle0 function
author: windows-sdk-content
description: Creates a handle used to enumerate a set of session objects.
old-location: fwp\fwpmsessioncreateenumhandle0_func.htm
old-project: FWP
ms.assetid: 018944eb-698b-4d3e-a9ba-253b8bbebea7
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmSessionCreateEnumHandle0, FwpmSessionCreateEnumHandle0 function [Filtering], fwp.fwpmsessioncreateenumhandle0_func, fwpmu/FwpmSessionCreateEnumHandle0
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
-	FwpmSessionCreateEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmSessionCreateEnumHandle0 function


## -description


The <b>FwpmSessionCreateEnumHandle0</b> function   creates a handle used to enumerate a set of session objects.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/d95fff0c-2f80-4ae4-9d75-9c7b0220a902">FWPM_SESSION_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle for filter enumeration.


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



If <i>enumTemplate</i> is <b>NULL</b>, all session objects are returned.

The caller must free the returned handle by a call to the <a href="https://msdn.microsoft.com/468793d1-451d-4116-b635-f45edff10211">FwpmSessionDestroyEnumHandle0</a>.

<b>FwpmSessionCreateEnumHandle0</b> cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the filter engine. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmSessionCreateEnumHandle0</b> is a specific implementation of FwpmSessionCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/d95fff0c-2f80-4ae4-9d75-9c7b0220a902">FWPM_SESSION_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/468793d1-451d-4116-b635-f45edff10211">FwpmSessionDestroyEnumHandle0</a>
 

 

