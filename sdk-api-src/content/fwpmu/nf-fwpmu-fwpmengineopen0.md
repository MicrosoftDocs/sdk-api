---
UID: NF:fwpmu.FwpmEngineOpen0
title: FwpmEngineOpen0 function
author: windows-sdk-content
description: Opens a session to the filter engine.
old-location: fwp\fwpmengineopen0_func.htm
tech.root: fwp
ms.assetid: 5165f219-f3e0-4e84-915b-75912aab02b7
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FwpmEngineOpen0, FwpmEngineOpen0 function [Filtering], fwp.fwpmengineopen0_func, fwpmu/FwpmEngineOpen0
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
 - FwpmEngineOpen0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FwpmEngineOpen0
: 
---

# FwpmEngineOpen0 function


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

Type: <b><a href="https://msdn.microsoft.com/829dee24-aeeb-4191-b5fc-85970725f064">SEC_WINNT_AUTH_IDENTITY_W</a>*</b>

The authentication and authorization credentials for accessing the filter engine. This pointer is optional and can be <b>NULL</b>. If this pointer is <b>NULL</b>, the calling thread's credentials are used.


### -param session [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/9f259ab7-cec9-44c1-8914-2850235470b3">FWPM_SESSION0</a>*</b>

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



A user application must call <b>FwpmEngineOpen0</b> to obtain a handle for open session to the filter engine before adding or removing any filter objects. A handle for an open session to the filter engine is also required for most of the other Windows Filtering Platform management functions.

The session is automatically closed when the program ends. To explicitly close a session, call <a href="https://msdn.microsoft.com/e96165a8-95ad-4cb0-9f45-e8af22f83a52">FwpmEngineClose0</a>.

If <i>session</i>.<b>flags</b> is set to <b>FWPM_SESSION_FLAG_DYNAMIC</b>, any WFP objects added during the session are
automatically deleted when the session ends. If the session is not dynamic, the caller needs to explicitly delete all WFP objects added during the session.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_OPEN</a> access to the filter engine. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmEngineOpen0</b> is intended for use in non-impersonated mode only.

<b>FwpmEngineOpen0</b> is a specific implementation of FwpmEngineOpen. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example uses <b>FwpmEngineOpen0</b> to open a filter session.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Open a session to the filter engine
        
HANDLE    engineHandle = NULL;
DWORD    result = ERROR_SUCCESS; 

printf("Opening the filter engine.\n");
        
result = FwpmEngineOpen0(
    NULL, 
    RPC_C_AUTHN_WINNT, 
    NULL,
    NULL, 
    &amp;engineHandle );

if (result != ERROR_SUCCESS)
    printf("FwpmEngineOpen0 failed. Return value: %d.\n", result); 
else
    printf("Filter engine opened successfully.\n");

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ac95276f-230d-4993-92fe-1739d022c8b3">Authentication-Service Constants</a>



<a href="https://msdn.microsoft.com/9f259ab7-cec9-44c1-8914-2850235470b3">FWPM_SESSION0</a>



<a href="https://msdn.microsoft.com/e96165a8-95ad-4cb0-9f45-e8af22f83a52">FwpmEngineClose0</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=98333">Kernel-Mode FwpmEngineOpen0</a>



<a href="https://msdn.microsoft.com/829dee24-aeeb-4191-b5fc-85970725f064">SEC_WINNT_AUTH_IDENTITY_W</a>
 

 

