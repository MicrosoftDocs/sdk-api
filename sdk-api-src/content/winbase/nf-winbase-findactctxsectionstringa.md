---
UID: NF:winbase.FindActCtxSectionStringA
title: FindActCtxSectionStringA function (winbase.h)
description: The FindActCtxSectionString function retrieves information on a specific string in the current activation context and returns a ACTCTX_SECTION_KEYED_DATA structure. (ANSI)
helpviewer_keywords: ["FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX", "FindActCtxSectionStringA", "winbase/FindActCtxSectionStringA"]
old-location: setup\findactctxsectionstring.htm
tech.root: setup
ms.assetid: d3f0b057-44ec-47ec-a0aa-69f3540b8900
ms.date: 12/05/2018
ms.keywords: FIND_ACTCTX_SECTION_KEY_RETURN_HACTCTX, FindActCtxSectionString, FindActCtxSectionString function [Side-by-side Assemblies], FindActCtxSectionStringA, FindActCtxSectionStringW, _win32_findactctxsectionstring, setup.findactctxsectionstring, winbase/FindActCtxSectionString, winbase/FindActCtxSectionStringA, winbase/FindActCtxSectionStringW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindActCtxSectionStringW (Unicode) and FindActCtxSectionStringA (ANSI)
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
 - FindActCtxSectionStringA
 - winbase/FindActCtxSectionStringA
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
 - API-Ms-Win-Core-Sidebyside-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - FindActCtxSectionString
 - FindActCtxSectionStringA
 - FindActCtxSectionStringW
---

# FindActCtxSectionStringA function


## -description

The 
<b>FindActCtxSectionString</b> function retrieves information on a specific string in the current activation context and returns a 
<a href="/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a> structure.

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
<a href="/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a> structure. The caller must use 
<a href="/windows/desktop/api/winbase/nf-winbase-releaseactctx">ReleaseActCtx</a> to release this activation context.

</td>
</tr>
</table>

### -param lpExtensionGuid [in]

Reserved; must be null.

### -param ulSectionId [in]

Identifier of the string section of the activation context in which to search for the specific string. 




The following are valid string section identifiers:

<ul>
<li>ACTIVATION_CONTEXT_SECTION_ASSEMBLY_INFORMATION</li>
<li>ACTIVATION_CONTEXT_SECTION_DLL_REDIRECTION</li>
<li>ACTIVATION_CONTEXT_SECTION_WINDOW_CLASS_REDIRECTION</li>
<li>ACTIVATION_CONTEXT_SECTION_COM_PROGID_REDIRECTION</li>
</ul>

### -param lpStringToFind [in]

Pointer to a null-terminated string to be used as the search criteria.

### -param ReturnedData [out]

Pointer to an 
<a href="/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a> structure to be filled out with the requested string information.

## -returns

If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function should only be called by the Side-by-side API functions or COM methods. Applications should not directly call this function.





> [!NOTE]
> The winbase.h header defines FindActCtxSectionString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findactctxsectionguid">FindActCtxSectionGuid</a>
