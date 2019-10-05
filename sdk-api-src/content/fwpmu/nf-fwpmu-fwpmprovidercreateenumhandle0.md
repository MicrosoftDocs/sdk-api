---
UID: NF:fwpmu.FwpmProviderCreateEnumHandle0
title: FwpmProviderCreateEnumHandle0 function (fwpmu.h)
author: windows-sdk-content
description: Creates a handle used to enumerate a set of providers.
old-location: fwp\fwpmprovidercreateenumhandle0_func.htm
tech.root: fwp
ms.assetid: f32d728d-eacc-4027-a1b1-31272425fd26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FwpmProviderCreateEnumHandle0, FwpmProviderCreateEnumHandle0 function [Filtering], fwp.fwpmprovidercreateenumhandle0_func, fwpmu/FwpmProviderCreateEnumHandle0
ms.topic: function
f1_keywords: 
 - "fwpmu/FwpmProviderCreateEnumHandle0"
dev_langs:
 - c++
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
 - FwpmProviderCreateEnumHandle0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmProviderCreateEnumHandle0 function


## -description


The <b>FwpmProviderCreateEnumHandle0</b> function creates a handle used to enumerate a set of providers.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0_">FWPM_PROVIDER_ENUM_TEMPLATE0</a>*</b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to  <b>FwpmProviderCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call  <b>FwpmProviderCreateEnumHandle0</b> and <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmproviderenum0">FwpmProviderEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmproviderdestroyenumhandle0">FwpmProviderDestroyEnumHandle0</a>.

The caller needs <a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ENUM</a> access to the providers' containers and <b>FWPM_ACTRL_READ</b> access to the providers. Only providers to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmProviderCreateEnumHandle0</b> is a specific implementation of FwpmProviderCreateEnumHandle. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0_">FWPM_PROVIDER_ENUM_TEMPLATE0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmproviderdestroyenumhandle0">FwpmProviderDestroyEnumHandle0</a>
 

 

