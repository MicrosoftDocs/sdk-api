---
UID: NF:winbase.FindActCtxSectionGuid
title: FindActCtxSectionGuid function (winbase.h)
description: The FindActCtxSectionGuid function retrieves information on a specific GUID in the current activation context and returns a ACTCTX_SECTION_KEYED_DATA structure.helpviewer_keywords: ["FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX","FindActCtxSectionGuid","FindActCtxSectionGuid function [Side-by-side Assemblies]","_win32_findactctxsectionguid","setup.findactctxsectionguid","winbase/FindActCtxSectionGuid"]
old-location: setup\findactctxsectionguid.htm
tech.root: SbsCs
ms.assetid: 3889505c-29a0-49dd-aca8-a26417b25a94
ms.date: 12/05/2018
ms.keywords: FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX, FindActCtxSectionGuid, FindActCtxSectionGuid function [Side-by-side Assemblies], _win32_findactctxsectionguid, setup.findactctxsectionguid, winbase/FindActCtxSectionGuid
f1_keywords:
- winbase/FindActCtxSectionGuid
dev_langs:
- c++
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
- FindActCtxSectionGuid
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FindActCtxSectionGuid function


## -description


The 
<b>FindActCtxSectionGuid</b> function retrieves information on a specific GUID in the current activation context and returns a 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a> structure.


## -parameters




### -param dwFlags [in]

Flags that determine how this function is to operate. Only the following flag is currently defined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX"></a><a id="find_actctx_section_key_return_hactctx"></a><dl>
<dt><b>FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX</b></dt>
</dl>
</td>
<td width="60%">
This function returns the activation context handle where the redirection data was found in the <b>hActCtx</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a> structure. The caller must use 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-releaseactctx">ReleaseActCtx</a> to release this activation context.

</td>
</tr>
</table>
 


### -param lpExtensionGuid [in]

Reserved; must be null.


### -param ulSectionId [in]

Identifier of the section of the activation context in which to search for the specified GUID. 




The following are valid GUID section identifiers:

<ul>
<li>ACTIVATION_CONTEXT_SECTION_COM_SERVER_REDIRECTION</li>
<li>ACTIVATION_CONTEXT_SECTION_COM_INTERFACE_REDIRECTION</li>
<li>ACTIVATION_CONTEXT_SECTION_COM_TYPE_LIBRARY_REDIRECTION</li>
</ul>
The following is a valid GUID section identifier beginning with Windows Server 2003 and Windows XP with SP1:

<ul>
<li>ACTIVATION_CONTEXT_SECTION_CLR_SURROGATES</li>
</ul>

### -param lpGuidToFind [in]

Pointer to a GUID to be used as the search criteria.


### -param ReturnedData [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a> structure to be filled out with the requested GUID information.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



This function should only be called by the Side-by-side API functions or COM methods. Applications should not directly call this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-findactctxsectionstringa">FindActCtxSectionString</a>
 

 

