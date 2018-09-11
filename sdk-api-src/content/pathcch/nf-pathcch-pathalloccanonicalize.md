---
UID: NF:pathcch.PathAllocCanonicalize
title: PathAllocCanonicalize function
author: windows-sdk-content
description: Converts a path string into a canonical form.This function differs from PathCchCanonicalize and PathCchCanonicalizeEx in that it returns the result on the heap.
old-location: shell\PathAllocCanonicalize.htm
tech.root: shell
ms.assetid: 3179fe78-a969-4ee2-a50b-5f4f7d4dad71
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: PATHCCH_ALLOW_LONG_PATHS, PATHCCH_DO_NOT_NORMALIZE_SEGMENTS, PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH, PATHCCH_ENSURE_TRAILING_SLASH, PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS, PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS, PATHCCH_NONE, PathAllocCanonicalize, PathAllocCanonicalize function [Windows Shell], pathcch/PathAllocCanonicalize, shell.PathAllocCanonicalize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pathcch.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - pathcch.lib
 - API-MS-Win-Core-Path-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PathAllocCanonicalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathAllocCanonicalize function


## -description



Converts a path string into a canonical form.

This function differs from <a href="https://msdn.microsoft.com/25ff08b2-5978-4d44-9877-ba4230ef7d12">PathCchCanonicalize</a> and <a href="https://msdn.microsoft.com/fd7b8ce0-3c67-48fb-8e7e-521a6b438676">PathCchCanonicalizeEx</a> in that it returns the result on the heap. This means that the caller does not have to declare the size of the returned string and reduces stack use.

This function differs from <a href="https://msdn.microsoft.com/e9b1e877-2cd6-4dd9-a15b-676cb940daed">PathCanonicalize</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, <a href="https://msdn.microsoft.com/25ff08b2-5978-4d44-9877-ba4230ef7d12">PathCchCanonicalize</a>, or <a href="https://msdn.microsoft.com/fd7b8ce0-3c67-48fb-8e7e-521a6b438676">PathCchCanonicalizeEx</a>, should be used in place of <a href="https://msdn.microsoft.com/e9b1e877-2cd6-4dd9-a15b-676cb940daed">PathCanonicalize</a>.</div><div> </div>

## -parameters




### -param pszPathIn [in]

A pointer to a buffer that contains the original string. This value cannot be <b>NULL</b>.


### -param dwFlags [in]

One or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_NONE"></a><a id="____pathcch_none"></a><dl>
<dt><b>    PATHCCH_NONE</b></dt>
<dt>0x0000000</dt>
</dl>
</td>
<td width="60%">
Do not allow for the construction of \\?\ paths (ie, long paths) longer than MAX_PATH. 

</td>
</tr>
<tr>
<td width="40%"><a id="PATHCCH_ALLOW_LONG_PATHS"></a><a id="pathcch_allow_long_paths"></a><dl>
<dt><b>PATHCCH_ALLOW_LONG_PATHS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Allow the building of \\?\ paths longer than MAX_PATH. 

</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_enable_long_name_process"></a><dl>
<dt><b>    PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Forces the API to treat the caller as long path enabled, independent of the 

    process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with 
<b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b>. 


<b>Note</b>  This value is available starting in Windows 10, version 1703.

</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_disable_long_name_process"></a><dl>
<dt><b>    PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Forces the API to treat the caller as long path disabled, independent of the 

    process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b>. 


<b>Note</b>  This value is available starting in Windows 10, version 1703.

</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_DO_NOT_NORMALIZE_SEGMENTS"></a><a id="____pathcch_do_not_normalize_segments"></a><dl>
<dt><b>    PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Disables the normalization of path segments that includes removing trailing dots and spaces. 

    This enables access to paths that win32 path normalization will block. 


<b>Note</b>  This value is available starting in Windows 10, version 1703.

</td>
</tr>
<tr>
<td width="40%"><a id="________PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH"></a><a id="________pathcch_ensure_is_extended_length_path"></a><dl>
<dt><b>        PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
    Converts the input path into the extended length DOS device path form (with the \\?\ prefix) 

    f not already in that form. This enables access to paths that are otherwise not addressable 

    due to Win32 normalization rules (that can strip trailing dots and spaces) and path 

    length limitations. This option implies the same behavior of <b>PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b>. 


<b>Note</b>  This value is available starting in Windows 10, version 1703.

</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_ENSURE_TRAILING_SLASH"></a><a id="____pathcch_ensure_trailing_slash"></a><dl>
<dt><b>    PATHCCH_ENSURE_TRAILING_SLASH</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
    When combining or normalizing a path, ensure there is a trailing backslash.

<b>Note</b>  This value is available starting in Windows 10, version 1703.

</td>
</tr>
</table>
 


### -param ppszPathOut [out]

The address of a pointer to a buffer that, when this function returns successfully, receives the canonicalized path string. It is the responsibility of the caller to free this resource, when it is no longer needed, by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function. This value cannot be <b>NULL</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function supports these alternate path forms:
            
                

<ul>
<li>\\?\</li>
<li>\\?\\UNC\</li>
<li>\\?\Volume{guid}\</li>
</ul>


