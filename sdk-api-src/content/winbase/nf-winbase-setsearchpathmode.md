---
UID: NF:winbase.SetSearchPathMode
title: SetSearchPathMode function (winbase.h)
description: Sets the per-process mode that the SearchPath function uses when locating files.
helpviewer_keywords: ["BASE_SEARCH_PATH_DISABLE_SAFE_SEARCHMODE","BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE","BASE_SEARCH_PATH_PERMANENT","SetSearchPathMode","SetSearchPathMode function [Files]","fs.setsearchpathmode","winbase/SetSearchPathMode"]
old-location: fs\setsearchpathmode.htm
tech.root: fs
ms.assetid: 1874933d-92c3-4945-a3e4-e6dede232d5e
ms.date: 12/05/2018
ms.keywords: BASE_SEARCH_PATH_DISABLE_SAFE_SEARCHMODE, BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE, BASE_SEARCH_PATH_PERMANENT, SetSearchPathMode, SetSearchPathMode function [Files], fs.setsearchpathmode, winbase/SetSearchPathMode
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.redist: KB959426 on      Windows XP with SP2 and later and Windows Server 2003 with SP1 and later
ms.custom: 19H1
f1_keywords:
 - SetSearchPathMode
 - winbase/SetSearchPathMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - SetSearchPathMode
---

# SetSearchPathMode function


## -description

Sets the per-process mode that the <a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> 
    function uses when locating files.

## -parameters

### -param Flags [in]

The search mode to use.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE"></a><a id="base_search_path_enable_safe_searchmode"></a><dl>
<dt><b>BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enable safe process search mode for the process.

</td>
</tr>
<tr>
<td width="40%"><a id="BASE_SEARCH_PATH_DISABLE_SAFE_SEARCHMODE"></a><a id="base_search_path_disable_safe_searchmode"></a><dl>
<dt><b>BASE_SEARCH_PATH_DISABLE_SAFE_SEARCHMODE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Disable safe process search mode for the process.

</td>
</tr>
<tr>
<td width="40%"><a id="BASE_SEARCH_PATH_PERMANENT"></a><a id="base_search_path_permanent"></a><dl>
<dt><b>BASE_SEARCH_PATH_PERMANENT</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Optional flag to use in combination with 
         <b>BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE</b> to make this mode permanent for this 
         process. This is done by bitwise <b>OR</b> operation:

<code>(BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE | BASE_SEARCH_PATH_PERMANENT)</code>

This flag cannot be combined with the <b>BASE_SEARCH_PATH_DISABLE_SAFE_SEARCHMODE</b> 
        flag.

</td>
</tr>
</table>

## -returns

If the operation completes successfully, the 
       <b>SetSearchPathMode</b> function returns a nonzero 
       value.

If the operation fails, the <b>SetSearchPathMode</b> 
       function returns zero. To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If the <b>SetSearchPathMode</b> function fails because a 
       parameter value is not valid, the value returned by the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function will be 
       <b>ERROR_INVALID_PARAMETER</b>.

If the <b>SetSearchPathMode</b> function fails because 
       the combination of current state and parameter value is not valid, the value returned by the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function will be 
       <b>ERROR_ACCESS_DENIED</b>. For more information, see the Remarks section.

## -remarks

If the <b>SetSearchPathMode</b> function has not been 
    successfully called for the current process, the search mode used by the 
    <a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> function is obtained from the system registry. For 
    more information, see <a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a>.

After the <b>SetSearchPathMode</b> function has been 
    successfully called for the current process, the setting in the system registry is ignored in favor of the mode 
    most recently set successfully.

If the <b>SetSearchPathMode</b> function has been 
     successfully called for the current process with <i>Flags</i> set to 
     <code>(BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE | BASE_SEARCH_PATH_PERMANENT)</code>, 
     safe mode is set permanently for the calling process. Any subsequent calls to the 
     <b>SetSearchPathMode</b> function from within that process 
     that attempt to change the search mode will fail with <b>ERROR_ACCESS_DENIED</b> from the 
     <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<div class="alert"><b>Note</b>  Because setting safe search mode permanently cannot be disabled for the life of the process for which is was 
     set, it should be used with careful consideration. This is particularly true for DLL development, where the user 
     of the DLL will be affected by this process-wide setting.</div>
<div> </div>
It is not possible to permanently disable safe search mode.

This function does not modify the system registry.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a>