---
UID: NF:fwpmu.FwpmProviderCreateEnumHandle0
title: FwpmProviderCreateEnumHandle0 function
author: windows-sdk-content
description: Creates a handle used to enumerate a set of providers.
old-location: fwp\fwpmprovidercreateenumhandle0_func.htm
old-project: FWP
ms.assetid: f32d728d-eacc-4027-a1b1-31272425fd26
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmProviderCreateEnumHandle0, FwpmProviderCreateEnumHandle0 function [Filtering], fwp.fwpmprovidercreateenumhandle0_func, fwpmu/FwpmProviderCreateEnumHandle0
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmProviderCreateEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmProviderCreateEnumHandle0 function


## -description


The <b>FwpmProviderCreateEnumHandle0</b> function creates a handle used to enumerate a set of providers.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/9369becc-f766-444a-8056-a3c3bc610553">FWPM_PROVIDER_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle for provider enumeration.


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



If <i>enumTemplate</i> is <b>NULL</b>, all providers are returned.

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to  <b>FwpmProviderCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call  <b>FwpmProviderCreateEnumHandle0</b> and <a href="https://msdn.microsoft.com/7c178688-64f4-49a9-907c-890f7d5030be">FwpmProviderEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to <a href="https://msdn.microsoft.com/a3402150-ea99-4456-b2c4-ab7643058861">FwpmProviderDestroyEnumHandle0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the providers' containers and <b>FWPM_ACTRL_READ</b> access to the providers. Only providers to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmProviderCreateEnumHandle0</b> is a specific implementation of FwpmProviderCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/9369becc-f766-444a-8056-a3c3bc610553">FWPM_PROVIDER_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/a3402150-ea99-4456-b2c4-ab7643058861">FwpmProviderDestroyEnumHandle0</a>
 

 

