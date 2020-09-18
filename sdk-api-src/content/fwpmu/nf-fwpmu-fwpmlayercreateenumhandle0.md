---
UID: NF:fwpmu.FwpmLayerCreateEnumHandle0
title: FwpmLayerCreateEnumHandle0 function (fwpmu.h)
description: Creates a handle used to enumerate a set of layer objects.
helpviewer_keywords: ["FwpmLayerCreateEnumHandle0","FwpmLayerCreateEnumHandle0 function [Filtering]","fwp.fwpmlayercreateenumhandle0_func","fwpmu/FwpmLayerCreateEnumHandle0"]
old-location: fwp\fwpmlayercreateenumhandle0_func.htm
tech.root: fwp
ms.assetid: 94738168-9f02-420a-96cd-b7c3f6418c6f
ms.date: 12/05/2018
ms.keywords: FwpmLayerCreateEnumHandle0, FwpmLayerCreateEnumHandle0 function [Filtering], fwp.fwpmlayercreateenumhandle0_func, fwpmu/FwpmLayerCreateEnumHandle0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmLayerCreateEnumHandle0
 - fwpmu/FwpmLayerCreateEnumHandle0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmLayerCreateEnumHandle0
---

# FwpmLayerCreateEnumHandle0 function


## -description

The <b>FwpmLayerCreateEnumHandle0</b> function creates a handle used to enumerate a set of layer objects.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumTemplate [in, optional]

Type: [FWPM_LAYER_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)*</b>

Template to selectively restrict the enumeration.

### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle for the layer enumeration.

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
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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

If <i>enumTemplate</i> is <b>NULL</b>, all layers are returned.

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to   <b>FwpmLayerCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call  <b>FwpmLayerCreateEnumHandle0</b> and <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmlayerenum0">FwpmLayerEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmlayerdestroyenumhandle0">FwpmLayerDestroyEnumHandle0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ENUM</a> access to the layers' containers and <b>FWPM_ACTRL_READ</b> access to the layers. Only layers to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmLayerCreateEnumHandle0</b> is a specific implementation of FwpmLayerCreateEnumHandle. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmlayerdestroyenumhandle0">FwpmLayerDestroyEnumHandle0</a>