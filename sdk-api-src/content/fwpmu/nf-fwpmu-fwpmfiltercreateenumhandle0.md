---
UID: NF:fwpmu.FwpmFilterCreateEnumHandle0
title: FwpmFilterCreateEnumHandle0 function
author: windows-sdk-content
description: Creates a handle used to enumerate a set of filter objects.
old-location: fwp\fwpmfiltercreateenumhandle0_func.htm
old-project: fwp
ms.assetid: fd8ffa91-a205-441c-9145-da8b441cef28
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FwpmFilterCreateEnumHandle0, FwpmFilterCreateEnumHandle0 function [Filtering], fwp.fwpmfiltercreateenumhandle0_func, fwpmu/FwpmFilterCreateEnumHandle0
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
 - FwpmFilterCreateEnumHandle0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmFilterCreateEnumHandle0 function


## -description


The <b>FwpmFilterCreateEnumHandle0</b> function creates a handle used to enumerate a set of filter objects.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/5ae77ee2-42b2-4794-afec-80360fe4f4da">FWPM_FILTER_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

The handle for filter enumeration.


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



If <i>enumTemplate</i> is <b>NULL</b>, all filters are returned.

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to  <b>FwpmFilterCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call <b>FwpmFilterCreateEnumHandle0</b> and <a href="https://msdn.microsoft.com/ced06ffd-668f-4d2b-b727-b705ad6a3149">FwpmFilterEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to <a href="https://msdn.microsoft.com/224ad984-8ab3-455b-8b20-019832325fa0">FwpmFilterDestroyEnumHandle0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the filters' containers and <b>FWPM_ACTRL_READ</b> access to the filters. Only filters to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmFilterCreateEnumHandle0</b> is a specific implementation of FwpmFilterCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/5ae77ee2-42b2-4794-afec-80360fe4f4da">FWPM_FILTER_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/224ad984-8ab3-455b-8b20-019832325fa0">FwpmFilterDestroyEnumHandle0</a>
 

 

