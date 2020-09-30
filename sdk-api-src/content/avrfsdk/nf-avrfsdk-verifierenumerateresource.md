---
UID: NF:avrfsdk.VerifierEnumerateResource
title: VerifierEnumerateResource function (avrfsdk.h)
description: Enumerates operating system resources for use by debugging and support tools.
helpviewer_keywords: ["AVRF_ENUM_RESOURCES_FLAGS_DONT_RESOLVE_TRACES","AVRF_ENUM_RESOURCES_FLAGS_SUSPEND","AvrfResourceHandleTrace","AvrfResourceHeapAllocation","VerifierEnumerateResource","VerifierEnumerateResource function [Windows API]","avrfsdk/VerifierEnumerateResource","base.verifierenumerateresource","winprog.verifierenumerateresource"]
old-location: winprog\verifierenumerateresource.htm
tech.root: winprog
ms.assetid: e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd
ms.date: 12/05/2018
ms.keywords: AVRF_ENUM_RESOURCES_FLAGS_DONT_RESOLVE_TRACES, AVRF_ENUM_RESOURCES_FLAGS_SUSPEND, AvrfResourceHandleTrace, AvrfResourceHeapAllocation, VerifierEnumerateResource, VerifierEnumerateResource function [Windows API], avrfsdk/VerifierEnumerateResource, base.verifierenumerateresource, winprog.verifierenumerateresource
req.header: avrfsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Verifier.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VerifierEnumerateResource
 - avrfsdk/VerifierEnumerateResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Verifier.dll
api_name:
 - VerifierEnumerateResource
---

# VerifierEnumerateResource function


## -description

Enumerates operating system resources for use by debugging and support tools.

## -parameters

### -param Process

A handle to the process in which resources are being enumerated.

When the <i>ResourceType</i> parameter is AvrfResrouceHeapAllocation, the handle must be opened with the PROCESS_VM_READ and PROCESS_QUERY_INFORMATION access rights.

If <i>ResourceType</i> is AvrfResrouceHeapAllocation and the <i>Flags</i> parameter contains AVRF_ENUM_RESOURCES_FLAGS_SUSPEND, the PROCESS_SUSPEND_RESUME flag must be used as well.

### -param Flags

If <i>ResourceType</i> is AvrfResourceHandleTrace, no flags are defined and the value for the Flags parameter must be 0.

If the <i>ResourceType</i> parameter is AvrfResourceHeapAllocation, the <i>Flags</i> parameter can be 0 or a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVRF_ENUM_RESOURCES_FLAGS_DONT_RESOLVE_TRACES"></a><a id="avrf_enum_resources_flags_dont_resolve_traces"></a><dl>
<dt><b>AVRF_ENUM_RESOURCES_FLAGS_DONT_RESOLVE_TRACES</b></dt>
</dl>
</td>
<td width="60%">
The stack backtraces of the heap allocations, when present, are not copied over the ReturnAddresses array. This may speed up the enumeration process.

</td>
</tr>
<tr>
<td width="40%"><a id="AVRF_ENUM_RESOURCES_FLAGS_SUSPEND"></a><a id="avrf_enum_resources_flags_suspend"></a><dl>
<dt><b>AVRF_ENUM_RESOURCES_FLAGS_SUSPEND</b></dt>
</dl>
</td>
<td width="60%">
The process is suspended before the heap allocations enumeration is executed.This minimizes the chance that changing the heap might affect the enumeration.

</td>
</tr>
</table>

### -param ResourceType

This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AvrfResourceHandleTrace"></a><a id="avrfresourcehandletrace"></a><a id="AVRFRESOURCEHANDLETRACE"></a><dl>
<dt><b>AvrfResourceHandleTrace</b></dt>
</dl>
</td>
<td width="60%">
The API enumerates the last recently saved operations on the handles from the handle table of the current process.

</td>
</tr>
<tr>
<td width="40%"><a id="AvrfResourceHeapAllocation"></a><a id="avrfresourceheapallocation"></a><a id="AVRFRESOURCEHEAPALLOCATION"></a><dl>
<dt><b>AvrfResourceHeapAllocation</b></dt>
</dl>
</td>
<td width="60%">
The API enumerates heap allocation, including heap metadata blocks.

</td>
</tr>
</table>

### -param ResourceCallback

An application-defined function that is invoked by the API.

The prototype is agnostic toward the type of resource being enumerated. The use will pass a prototype suitable for the type of enumeration being performed

### -param EnumerationContext

An application-specific pointer that is passed back to the callback function.

## -returns

This function returns one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Verifier.dll.


#### Examples

See <a href="/windows/desktop/DevNotes/using-resource-enumeration">Using Resource Enumeration</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/avrfsdk/nc-avrfsdk-avrf_handleoperation_enumerate_callback">AVRF_HANDLEOPERATION_ENUMERATE_CALLBACK</a>



<a href="/windows/desktop/api/avrfsdk/nc-avrfsdk-avrf_heapallocation_enumerate_callback">AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK</a>



<a href="/windows/desktop/api/avrfsdk/nc-avrfsdk-avrf_resource_enumerate_callback">AVRF_RESOURCE_ENUMERATE_CALLBACK</a>



<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>