---
UID: NF:fwpmu.FwpmSubLayerCreateEnumHandle0
title: FwpmSubLayerCreateEnumHandle0 function (fwpmu.h)
author: windows-sdk-content
description: Creates a handle used to enumerate a set of sublayers.
old-location: fwp\fwpmsublayercreateenumhandle0_func.htm
tech.root: fwp
ms.assetid: a8acff10-8395-4ef8-8976-7a99cd498a7d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FwpmSubLayerCreateEnumHandle0, FwpmSubLayerCreateEnumHandle0 function [Filtering], fwp.fwpmsublayercreateenumhandle0_func, fwpmu/FwpmSubLayerCreateEnumHandle0
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
 - FwpmSubLayerCreateEnumHandle0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmSubLayerCreateEnumHandle0 function


## -description


The <b>FwpmSubLayerCreateEnumHandle0</b> function   creates a handle used to enumerate a set of sublayers.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumTemplate [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4f05730c-7bf6-4bf4-b3ec-d8fe138b2228">FWPM_SUBLAYER_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.


### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle for sublayer enumeration.


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



If <i>enumTemplate</i> is <b>NULL</b>, all sublayers are returned.

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to   <b>FwpmSubLayerCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call <b>FwpmSubLayerCreateEnumHandle0</b> and <a href="https://msdn.microsoft.com/2f370d6f-4670-401e-840e-11f775dbd873">FwpmSubLayerEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to  <a href="https://msdn.microsoft.com/ad4e5a70-a29f-44ff-a70d-3fcb31972f90">FwpmSubLayerDestroyEnumHandle0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ENUM</a> access to the sublayers' containers and <b>FWPM_ACTRL_READ</b> access to the sub-layers. Only sublayers to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmSubLayerCreateEnumHandle0</b> is a specific implementation of FwpmSubLayerCreateEnumHandle. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/4f05730c-7bf6-4bf4-b3ec-d8fe138b2228">FWPM_SUBLAYER_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/ad4e5a70-a29f-44ff-a70d-3fcb31972f90">FwpmSubLayerDestroyEnumHandle0</a>
 

 

