---
UID: NF:fwpmu.FwpmEngineOpen0
title: FwpmEngineOpen0 function (fwpmu.h)
description: Opens a session to the filter engine.
helpviewer_keywords: ["FwpmEngineOpen0","FwpmEngineOpen0 function [Filtering]","fwp.fwpmengineopen0_func","fwpmu/FwpmEngineOpen0"]
old-location: fwp\fwpmengineopen0_func.htm
tech.root: fwp
ms.assetid: 5165f219-f3e0-4e84-915b-75912aab02b7
ms.date: 12/05/2018
ms.keywords: FwpmEngineOpen0, FwpmEngineOpen0 function [Filtering], fwp.fwpmengineopen0_func, fwpmu/FwpmEngineOpen0
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
 - FwpmEngineOpen0
 - fwpmu/FwpmEngineOpen0
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
 - FwpmEngineOpen0
---

## -description

The <b>FwpmEngineOpen0</b> function  opens a session to the filter engine.

## -parameters

### -param serverName [in, optional]

Type: <b>const wchar_t*</b>

This value must be <b>NULL</b>.

### -param authnService [in]

Type: <b>UINT32</b>

Specifies the authentication service to use. Allowed services are RPC_C_AUTHN_WINNT and RPC_C_AUTHN_DEFAULT.

### -param authIdentity [in, optional]

Type: <b><a href="/windows/win32/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY_A</a>*</b>

The authentication and authorization credentials for accessing the filter engine. This pointer is optional and can be <b>NULL</b>. If this pointer is <b>NULL</b>, the calling thread's credentials are used.

### -param session [in, optional]

Type: [FWPM_SESSION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_session0)*</b>

Session-specific parameters for the session being opened. This pointer is optional and can be <b>NULL</b>.

### -param engineHandle [out]

Type: <b>HANDLE*</b>

Handle for the open session to the filter engine.

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
The session was started successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_ALREADY_EXISTS</b></dt>
<dt>0x80320009</dt>
</dl>
</td>
<td width="60%">
A session with the specified <b>sessionKey</b> is already opened.

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

A user application must call <b>FwpmEngineOpen0</b> to obtain a handle for open session to the filter engine before adding or removing any filter objects. A handle for an open session to the filter engine is also required for most of the other Windows Filtering Platform management functions.

The session is automatically closed when the program ends. To explicitly close a session, call <a href="/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineclose0">FwpmEngineClose0</a>.

If <i>session</i>.<b>flags</b> is set to <b>FWPM_SESSION_FLAG_DYNAMIC</b>, any WFP objects added during the session are
automatically deleted when the session ends. If the session is not dynamic, the caller needs to explicitly delete all WFP objects added during the session.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_OPEN</a> access to the filter engine. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmEngineOpen0</b> is intended for use in non-impersonated mode only.

<b>FwpmEngineOpen0</b> is a specific implementation of FwpmEngineOpen. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example uses <b>FwpmEngineOpen0</b> to open a filter session.


```cpp
// Open a session to the filter engine
        
HANDLE    engineHandle = NULL;
DWORD    result = ERROR_SUCCESS; 

printf("Opening the filter engine.\n");
        
result = FwpmEngineOpen0(
    NULL, 
    RPC_C_AUTHN_WINNT, 
    NULL,
    NULL, 
    &engineHandle );

if (result != ERROR_SUCCESS)
    printf("FwpmEngineOpen0 failed. Return value: %d.\n", result); 
else
    printf("Filter engine opened successfully.\n");

```

## -see-also

<a href="/windows/desktop/Rpc/authentication-service-constants">Authentication-Service Constants</a>



[FWPM_SESSION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_session0)



<a href="/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineclose0">FwpmEngineClose0</a>



[Kernel-Mode FwpmEngineOpen0](nf-fwpmu-fwpmengineopen0.md)



<a href="/windows/win32/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY_A</a>
