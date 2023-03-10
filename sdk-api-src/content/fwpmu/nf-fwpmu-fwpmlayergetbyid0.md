---
UID: NF:fwpmu.FwpmLayerGetById0
title: FwpmLayerGetById0 function (fwpmu.h)
description: Retrieves a layer object. (FwpmLayerGetById0)
helpviewer_keywords: ["FwpmLayerGetById0","FwpmLayerGetById0 function [Filtering]","fwp.fwpmlayergetbyid0_func","fwpmu/FwpmLayerGetById0"]
old-location: fwp\fwpmlayergetbyid0_func.htm
tech.root: fwp
ms.assetid: c7668d06-8533-4dd1-a4f6-fb38c97219db
ms.date: 12/05/2018
ms.keywords: FwpmLayerGetById0, FwpmLayerGetById0 function [Filtering], fwp.fwpmlayergetbyid0_func, fwpmu/FwpmLayerGetById0
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
 - FwpmLayerGetById0
 - fwpmu/FwpmLayerGetById0
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
 - FwpmLayerGetById0
---

# FwpmLayerGetById0 function


## -description

The <b>FwpmLayerGetById0</b> function retrieves a layer object.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT16</b>

 Identifier of the desired layer. For a list of possible values, see <a href="/windows-hardware/drivers/network/run-time-filtering-layer-identifiers">Run-time Filtering Layer Identifiers</a>  in the WDK documentation for Windows Filtering Platform.

### -param layer [out]

Type: [FWPM_LAYER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_layer0)**</b>

The layer information.

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
The layer was retrieved successfully.

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

The caller must free the returned object by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the layer. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmLayerGetById0</b> is a specific implementation of FwpmLayerGetById. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_LAYER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_layer0)



<a href="/windows-hardware/drivers/network/run-time-filtering-layer-identifiers">Run-time Filtering Layer Identifiers</a>
