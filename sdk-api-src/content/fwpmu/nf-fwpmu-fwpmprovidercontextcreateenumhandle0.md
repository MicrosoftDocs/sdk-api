---
UID: NF:fwpmu.FwpmProviderContextCreateEnumHandle0
title: FwpmProviderContextCreateEnumHandle0 function
author: windows-driver-content
description: Creates a handle used to enumerate a set of provider contexts.
old-location: fwp\fwpmprovidercontextcreateenumhandle0_func.htm
old-project: FWP
ms.assetid: 3b660e3a-fba6-4466-aa82-eb90c27ae004
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FwpmProviderContextCreateEnumHandle0, FwpmProviderContextCreateEnumHandle0 function [Filtering], fwp.fwpmprovidercontextcreateenumhandle0_func, fwpmu/FwpmProviderContextCreateEnumHandle0
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmProviderContextCreateEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmProviderContextCreateEnumHandle0 function


## -description


The <b>FwpmProviderContextCreateEnumHandle0</b> function creates a handle used to enumerate a set of provider contexts.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0d43931a-93ae-43dd-9c5b-3989799e7b60">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle for provider context enumeration.


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



If <i>enumTemplate</i> is <b>NULL</b>, all provider contexts are returned.

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to  <b>FwpmProviderContextCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call <b>FwpmProviderContextCreateEnumHandle0</b> and <a href="https://msdn.microsoft.com/a086c9b3-5cec-4cea-9224-ba423302eba8">FwpmProviderContextEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to <a href="https://msdn.microsoft.com/85ec36f8-c6e0-4dcf-aad2-15d61aa6bd64">FwpmProviderContextDestroyEnumHandle0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the provider contexts' containers and <b>FWPM_ACTRL_READ</b> access to the provider contexts. Only provider contexts to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmProviderContextCreateEnumHandle0</b> is a specific implementation of FwpmProviderContextCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/0d43931a-93ae-43dd-9c5b-3989799e7b60">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/85ec36f8-c6e0-4dcf-aad2-15d61aa6bd64">FwpmProviderContextDestroyEnumHandle0</a>
 

 

