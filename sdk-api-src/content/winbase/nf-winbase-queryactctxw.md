---
UID: NF:winbase.QueryActCtxW
title: QueryActCtxW function (winbase.h)
description: The QueryActCtxW function queries the activation context.
helpviewer_keywords: ["ActivationContextBasicInformation","ActivationContextDetailedInformation","AssemblyDetailedInformationInActivationContext","CompatibilityInformationInActivationContext","FileInformationInAssemblyOfAssemblyInActivationContext","QUERY_ACTCTX_FLAG_ACTCTX_IS_ADDRESS","QUERY_ACTCTX_FLAG_ACTCTX_IS_HMODULE","QUERY_ACTCTX_FLAG_USE_ACTIVE_ACTCTX","QueryActCtxW","QueryActCtxW function [Side-by-side Assemblies]","RunlevelInformationInActivationContext","_win32_queryactctxw","setup.queryactctxw","winbase/QueryActCtxW"]
old-location: setup\queryactctxw.htm
tech.root: setup
ms.assetid: 7d45f63f-0baf-4236-b245-d36f9eb32e8c
ms.date: 12/05/2018
ms.keywords: ActivationContextBasicInformation, ActivationContextDetailedInformation, AssemblyDetailedInformationInActivationContext, CompatibilityInformationInActivationContext, FileInformationInAssemblyOfAssemblyInActivationContext, QUERY_ACTCTX_FLAG_ACTCTX_IS_ADDRESS, QUERY_ACTCTX_FLAG_ACTCTX_IS_HMODULE, QUERY_ACTCTX_FLAG_USE_ACTIVE_ACTCTX, QueryActCtxW, QueryActCtxW function [Side-by-side Assemblies], RunlevelInformationInActivationContext, _win32_queryactctxw, setup.queryactctxw, winbase/QueryActCtxW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryActCtxW
 - winbase/QueryActCtxW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-sidebyside-l1-1-0.dll
 - KernelBase.dll
api_name:
 - QueryActCtxW
---

# QueryActCtxW function


## -description

The 
<b>QueryActCtxW</b> function queries the activation context.

## -parameters

### -param dwFlags [in]

This parameter should be set to one of the following flag bits. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QUERY_ACTCTX_FLAG_USE_ACTIVE_ACTCTX"></a><a id="query_actctx_flag_use_active_actctx"></a><dl>
<dt><b>QUERY_ACTCTX_FLAG_USE_ACTIVE_ACTCTX</b></dt>
</dl>
</td>
<td width="60%">
<b>QueryActCtxW</b> queries the activation context active on the thread instead of the context specified by <i>hActCtx</i>. This is usually the last activation context passed to 
<a href="/windows/desktop/api/winbase/nf-winbase-activateactctx">ActivateActCtx</a>. If 
<b>ActivateActCtx</b> has not been called, the active activation context can be the activation context used by the executable of the current process. In other cases, the operating system  determines the active activation context. For example, when the callback function to a new thread is called, the active activation context may be the context that was active when you created the thread by calling <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="QUERY_ACTCTX_FLAG_ACTCTX_IS_HMODULE"></a><a id="query_actctx_flag_actctx_is_hmodule"></a><dl>
<dt><b>QUERY_ACTCTX_FLAG_ACTCTX_IS_HMODULE</b></dt>
</dl>
</td>
<td width="60%">
<b>QueryActCtxW</b> interprets <i>hActCtx</i> as an <b>HMODULE</b> data type and queries an activation context that is associated with a DLL or EXE. 




When a DLL or EXE is loaded, the loader checks for a manifest stored in a resource. If the loader finds an RT_MANIFEST resource with a resource identifier set to ISOLATIONAWARE_MANIFEST_ RESOURCE_ID, the loader associates the resulting activation context with the DLL or EXE. This is the activation context that 
<b>QueryActCtxW</b> queries when the QUERY_ACTCTX_FLAG_ACTCTX_IS_HMODULE flag has been set.

</td>
</tr>
<tr>
<td width="40%"><a id="QUERY_ACTCTX_FLAG_ACTCTX_IS_ADDRESS"></a><a id="query_actctx_flag_actctx_is_address"></a><dl>
<dt><b>QUERY_ACTCTX_FLAG_ACTCTX_IS_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
<b>QueryActCtxW</b> interprets <i>hActCtx</i> as an address within a DLL or EXE and queries an activation context that has been associated with the DLL or EXE. This can be any address within the DLL or EXE. For example, the address of any function within a DLL or EXE or the address of any static data, such as a constant string. 




When a DLL or EXE is loaded, the loader checks for a manifest stored in a resource in the same way as QUERY_ACTCTX_FLAG_ACTCTX_IS_HMODULE.

</td>
</tr>
</table>

### -param hActCtx [in]

Handle to the activation context that is being queried.

### -param pvSubInstance [in, optional]

Index of the assembly, or assembly and file combination, in the activation context. The meaning of the <i>pvSubInstance</i> depends on the option specified by the value of the <i>ulInfoClass</i> parameter. 

 This parameter may be null.

<table>
<tr>
<th>ulInfoClass Option</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AssemblyDetailedInformationInActivationContext"></a><a id="assemblydetailedinformationinactivationcontext"></a><a id="ASSEMBLYDETAILEDINFORMATIONINACTIVATIONCONTEXT"></a><dl>
<dt><b>AssemblyDetailedInformationInActivationContext</b></dt>
</dl>
</td>
<td width="60%">
Pointer to a <b>DWORD</b> that specifies the index of the assembly within the activation context. This is the activation context that 
<b>QueryActCtxW</b> queries.

</td>
</tr>
<tr>
<td width="40%"><a id="FileInformationInAssemblyOfAssemblyInActivationContext"></a><a id="fileinformationinassemblyofassemblyinactivationcontext"></a><a id="FILEINFORMATIONINASSEMBLYOFASSEMBLYINACTIVATIONCONTEXT"></a><dl>
<dt><b>FileInformationInAssemblyOfAssemblyInActivationContext</b></dt>
</dl>
</td>
<td width="60%">
Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-activation_context_query_index">ACTIVATION_CONTEXT_QUERY_INDEX</a> structure. If 
<b>QueryActCtxW</b> is called with this option and the function succeeds, the returned buffer contains information for a file in the assembly. This information is in the form of the 
<a href="/windows/desktop/api/winnt/ns-winnt-assembly_file_detailed_information">ASSEMBLY_FILE_DETAILED_INFORMATION</a> structure.

</td>
</tr>
</table>

### -param ulInfoClass [in]

This parameter can have only the values shown in the following table. 



<table>
<tr>
<th>Option</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ActivationContextBasicInformation"></a><a id="activationcontextbasicinformation"></a><a id="ACTIVATIONCONTEXTBASICINFORMATION"></a><dl>
<dt><b>ActivationContextBasicInformation</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Not available.

</td>
</tr>
<tr>
<td width="40%"><a id="ActivationContextDetailedInformation"></a><a id="activationcontextdetailedinformation"></a><a id="ACTIVATIONCONTEXTDETAILEDINFORMATION"></a><dl>
<dt><b>ActivationContextDetailedInformation</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
If 
<b>QueryActCtxW</b> is called with this option and the function succeeds, the returned buffer contains detailed information about the activation context. This information is in the form of the 
<a href="/windows/win32/api/winnt/ns-winnt-activation_context_detailed_information">ACTIVATION_CONTEXT_DETAILED_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="AssemblyDetailedInformationInActivationContext"></a><a id="assemblydetailedinformationinactivationcontext"></a><a id="ASSEMBLYDETAILEDINFORMATIONINACTIVATIONCONTEXT"></a><dl>
<dt><b>AssemblyDetailedInformationInActivationContext</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
If 
<b>QueryActCtxW</b> is called with this option and the function succeeds, the buffer contains information about the assembly that has the index specified in <i>pvSubInstance</i>. This information is in the form of the 
<a href="/windows/win32/api/winnt/ns-winnt-activation_context_assembly_detailed_information">ACTIVATION_CONTEXT_ASSEMBLY_DETAILED_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="FileInformationInAssemblyOfAssemblyInActivationContext"></a><a id="fileinformationinassemblyofassemblyinactivationcontext"></a><a id="FILEINFORMATIONINASSEMBLYOFASSEMBLYINACTIVATIONCONTEXT"></a><dl>
<dt><b>FileInformationInAssemblyOfAssemblyInActivationContext</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Information about a file in one of the assemblies in Activation Context. The <i>pvSubInstance</i> parameter must point to an 
<a href="/windows/desktop/api/winnt/ns-winnt-activation_context_query_index">ACTIVATION_CONTEXT_QUERY_INDEX</a> structure. If 
<b>QueryActCtxW</b> is called with this option and the function succeeds, the returned buffer contains information for a file in the assembly. This information is in the form of the 
<a href="/windows/desktop/api/winnt/ns-winnt-assembly_file_detailed_information">ASSEMBLY_FILE_DETAILED_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RunlevelInformationInActivationContext"></a><a id="runlevelinformationinactivationcontext"></a><a id="RUNLEVELINFORMATIONINACTIVATIONCONTEXT"></a><dl>
<dt><b>RunlevelInformationInActivationContext</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
If 
<b>QueryActCtxW</b> is called with this option and the function succeeds, the buffer contains information about requested run level of the activation context. This information is in the form of the 
<a href="/windows/win32/api/winnt/ns-winnt-activation_context_run_level_information">ACTIVATION_CONTEXT_RUN_LEVEL_INFORMATION</a> structure.

<b>Windows Server 2003 and Windows XP:  </b>This value is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="CompatibilityInformationInActivationContext"></a><a id="compatibilityinformationinactivationcontext"></a><a id="COMPATIBILITYINFORMATIONINACTIVATIONCONTEXT"></a><dl>
<dt><b>CompatibilityInformationInActivationContext</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
If 
<b>QueryActCtxW</b> is called with this option and the function succeeds, the buffer contains information about requested compatibility context. This information is in the form of the 
<a href="/windows/win32/api/winnt/ns-winnt-activation_context_compatibility_information">ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION</a> structure.

<b>Windows Server 2008 and earlier, and Windows Vista and earlier:  </b>This value is not available. This option is available beginning with Windows Server 2008 R2 and Windows 7.

</td>
</tr>
</table>

### -param pvBuffer [out]

Pointer to a buffer that holds the returned information. This parameter is optional. If <i>pvBuffer</i> is <b>null</b>, then <i>cbBuffer</i> must be zero. If the size of the buffer pointed to by <i>pvBuffer</i> is too small, 
<b>QueryActCtxW</b> returns ERROR_INSUFFICIENT_BUFFER and no data is written into the buffer. See the Remarks section for the method you can use to determine the required size of the buffer.

### -param cbBuffer [in, optional]

Size of the buffer in bytes pointed to by <i>pvBuffer</i>. This parameter is optional.

### -param pcbWrittenOrRequired [out, optional]

Number of bytes written or required. The parameter <i>pcbWrittenOrRequired</i> can only be <b>NULL</b> when <i>pvBuffer</i> is <b>NULL</b>. If <i>pcbWrittenOrRequired</i> is non-<b>NULL</b>, it is filled with the number of bytes required to store the returned buffer.

## -returns

If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The parameter <i>cbBuffer</i> specifies the size in bytes of the buffer pointed to by <i>pvBuffer</i>. If <i>pvBuffer</i> is <b>NULL</b>, then <i>cbBuffer</i> must be 0. The parameter <i>pcbWrittenOrRequired</i> can only be <b>NULL</b> if <i>pvBuffer</i> is <b>NULL</b>. If <i>pcbWrittenOrRequired</i> is non-<b>NULL</b> on return, it is filled with the number of bytes required to store the returned information. When the information data returned is larger than the provided buffer, 
<b>QueryActCtxW</b> returns ERROR_INSUFFICIENT_BUFFER and no data is written to the buffer pointed to by <i>pvBuffer</i>.

The following example shows the method of calling first with a small buffer and then recalling if the buffer is too small.


``` syntax
SIZE_T cbRequired;
PVOID pvData = NULL;
SIZE_T cbAvailable = 0;

if (!QueryActCtxW(..., pvData, cbAvailable, &cbRequired) && (GetLastError()== ERROR_INSUFFICIENT_BUFFER))
{
    // Allocate enough space to store the returned buffer, fail if too small
    if (NULL == (pvData = HeapAlloc(GetProcessHeap(), 0, cbRequired)))
    {
        SetLastError(ERROR_NOT_ENOUGH_MEMORY);
        return FALSE;
    }
    cbAvailable = cbRequired;
    // Try again, this should succeed.
    if (QueryActCtxW(..., pvData, cbAvailable, &cbRequired))
    {
        // Use the returned data in pvData
    }
    HeapFree(GetProcessHeap(), 0, pvData);
    pvData = NULL;
}
```

