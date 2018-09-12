---
UID: NF:fwpmu.FwpmSubLayerAdd0
title: FwpmSubLayerAdd0 function
author: windows-sdk-content
description: Adds a new sublayer to the system.
old-location: fwp\fwpmsublayeradd0_func.htm
tech.root: fwp
ms.assetid: 85a6f4a9-297f-491d-b2f7-38de21dbe06c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FwpmSubLayerAdd0, FwpmSubLayerAdd0 function [Filtering], fwp.fwpmsublayeradd0_func, fwpmu/FwpmSubLayerAdd0
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
 - FwpmSubLayerAdd0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmSubLayerAdd0 function


## -description


The <b>FwpmSubLayerAdd0</b> function adds a new sublayer to the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subLayer [in]

Type: <b>const <a href="https://msdn.microsoft.com/ce689b1d-1f5c-4dde-96cd-9001de3827aa">FWPM_SUBLAYER0</a>*</b>

The sublayer to be added.


### -param sd [in, optional]

Type: <b><a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">PSECURITY_DESCRIPTOR</a></b>

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



If the caller supplies a null security descriptor, the system will assign a default security descriptor.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ADD</a> access to the sublayers's container and <b>FWPM_ACTRL_ADD_LINK</b> access to the provider (if any).  See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmSubLayerAdd0</b> is a specific implementation of FwpmSubLayerAdd. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example illustrates initialization of a sublayer object and adding the sublayer key to a filter object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;fwpmu.h&gt;
#include &lt;rpc.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "Fwpuclnt.lib")
#pragma comment(lib, "Rpcrt4.lib")

void main()
{
    FWPM_FILTER0    fwpFilter;
    FWPM_SUBLAYER0    fwpFilterSubLayer;
    HANDLE engineHandle = NULL;     
    DWORD  result = ERROR_SUCCESS; 
    RPC_STATUS rpcStatus = RPC_S_OK;
     
    memset(&amp;fwpFilterSubLayer, 0, sizeof(fwpFilterSubLayer));
    rpcStatus = UuidCreate(&amp;fwpFilterSubLayer.subLayerKey);
          
    if (RPC_S_OK != rpcStatus)
    {
           printf("UuidCreate failed (%d).\n", rpcStatus);
           return;
    }

    result = FwpmEngineOpen0( NULL, RPC_C_AUTHN_WINNT, NULL, NULL, &amp;engineHandle );
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
      result = FwpmSubLayerAdd0(engineHandle, &amp;fwpFilterSubLayer, NULL);

      if (result != ERROR_SUCCESS)
      {           
           printf("FwpmSubLayerAdd0 failed (%d).\n", result);
           return;
    }

    // Add sublayer key to a filter.
    memset(&amp;fwpFilter, 0, sizeof(FWPM_FILTER0));

    if (&amp;fwpFilterSubLayer.subLayerKey != NULL)
        fwpFilter.subLayerKey = fwpFilterSubLayer.subLayerKey;

    // Finish initializing filter...

    return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ce689b1d-1f5c-4dde-96cd-9001de3827aa">FWPM_SUBLAYER0</a>



<a href="https://msdn.microsoft.com/983eb1bb-af6b-42cf-8148-ed3a0e3102a9">Management Functions</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

