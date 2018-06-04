---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SetSearchPathMode function


## -description


Sets the per-process mode that the <a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a> 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

If the <b>SetSearchPathMode</b> function fails because a 
       parameter value is not valid, the value returned by the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function will be 
       <b>ERROR_INVALID_PARAMETER</b>.

If the <b>SetSearchPathMode</b> function fails because 
       the combination of current state and parameter value is not valid, the value returned by the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function will be 
       <b>ERROR_ACCESS_DENIED</b>. For more information, see the Remarks section.




## -remarks



If the <b>SetSearchPathMode</b> function has not been 
    successfully called for the current process, the search mode used by the 
    <a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a> function is obtained from the system registry. For 
    more information, see <a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a>.

After the <b>SetSearchPathMode</b> function has been 
    successfully called for the current process, the setting in the system registry is ignored in favor of the mode 
    most recently set successfully.

If the <b>SetSearchPathMode</b> function has been 
     successfully called for the current process with <i>Flags</i> set to 
     <code>(BASE_SEARCH_PATH_ENABLE_SAFE_SEARCHMODE | BASE_SEARCH_PATH_PERMANENT)</code>, 
     safe mode is set permanently for the calling process. Any subsequent calls to the 
     <b>SetSearchPathMode</b> function from within that process 
     that attempt to change the search mode will fail with <b>ERROR_ACCESS_DENIED</b> from the 
     <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

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




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a>
 

 

