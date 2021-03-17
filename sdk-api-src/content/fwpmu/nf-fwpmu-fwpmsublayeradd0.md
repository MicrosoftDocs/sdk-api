---
UID: NF:fwpmu.FwpmSubLayerAdd0
title: FwpmSubLayerAdd0 function (fwpmu.h)
description: Adds a new sublayer to the system.
helpviewer_keywords: ["FwpmSubLayerAdd0","FwpmSubLayerAdd0 function [Filtering]","fwp.fwpmsublayeradd0_func","fwpmu/FwpmSubLayerAdd0"]
old-location: fwp\fwpmsublayeradd0_func.htm
tech.root: fwp
ms.assetid: 85a6f4a9-297f-491d-b2f7-38de21dbe06c
ms.date: 12/05/2018
ms.keywords: FwpmSubLayerAdd0, FwpmSubLayerAdd0 function [Filtering], fwp.fwpmsublayeradd0_func, fwpmu/FwpmSubLayerAdd0
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
 - FwpmSubLayerAdd0
 - fwpmu/FwpmSubLayerAdd0
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
 - FwpmSubLayerAdd0
---

# FwpmSubLayerAdd0 function


## -description

The <b>FwpmSubLayerAdd0</b> function adds a new sublayer to the system.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param subLayer [in]

Type: [FWPM_SUBLAYER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)*</b>

The sublayer to be added.

### -param sd [in, optional]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a></b>

Security information for the sublayer object.

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
The sublayer was successfully added.

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

If the caller supplies a null security descriptor, the system will assign a default security descriptor.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD</a> access to the sublayers's container and <b>FWPM_ACTRL_ADD_LINK</b> access to the provider (if any).  See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmSubLayerAdd0</b> is a specific implementation of FwpmSubLayerAdd. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example illustrates initialization of a sublayer object and adding the sublayer key to a filter object.


```cpp
#include <windows.h>
#include <fwpmu.h>
#include <rpc.h>
#include <stdio.h>

#pragma comment(lib, "Fwpuclnt.lib")
#pragma comment(lib, "Rpcrt4.lib")

void main()
{
    FWPM_FILTER0    fwpFilter;
    FWPM_SUBLAYER0    fwpFilterSubLayer;
    HANDLE engineHandle = NULL;     
    DWORD  result = ERROR_SUCCESS; 
    RPC_STATUS rpcStatus = RPC_S_OK;
     
    memset(&fwpFilterSubLayer, 0, sizeof(fwpFilterSubLayer));
    rpcStatus = UuidCreate(&fwpFilterSubLayer.subLayerKey);
          
    if (RPC_S_OK != rpcStatus)
    {
           printf("UuidCreate failed (%d).\n", rpcStatus);
           return;
    }

    result = FwpmEngineOpen0( NULL, RPC_C_AUTHN_WINNT, NULL, NULL, &engineHandle );
    if (result != ERROR_SUCCESS)
    {
        printf("FwpmEngineOpen0 failed.\n");
        return;
    }

    fwpFilterSubLayer.displayData.name = L"MyFilterSublayer";
    fwpFilterSubLayer.displayData.description = L"My filter sublayer";
    fwpFilterSubLayer.flags = 0;
    fwpFilterSubLayer.weight = 0x100;
            
    printf("Adding filter sublayer.\n");
      result = FwpmSubLayerAdd0(engineHandle, &fwpFilterSubLayer, NULL);

      if (result != ERROR_SUCCESS)
      {           
           printf("FwpmSubLayerAdd0 failed (%d).\n", result);
           return;
    }

    // Add sublayer key to a filter.
    memset(&fwpFilter, 0, sizeof(FWPM_FILTER0));

    if (&fwpFilterSubLayer.subLayerKey != NULL)
        fwpFilter.subLayerKey = fwpFilterSubLayer.subLayerKey;

    // Finish initializing filter...

    return;
}

```

## -see-also

[FWPM_SUBLAYER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)



<a href="/windows/desktop/FWP/fwp-mgmt-functions">Management Functions</a>



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>