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

# GetProcessDEPPolicy function


## -description


Gets the data execution prevention (DEP) and DEP-ATL thunk emulation settings for the specified 32-bit process.<b>Windows XP with SP3:  </b>Gets the DEP and DEP-ATL thunk emulation settings for the current process. 




## -parameters




### -param hProcess [in]

A handle to the process. <b>PROCESS_QUERY_INFORMATION</b> privilege is required to get the DEP policy of a process. 

<b>Windows XP with SP3:  </b>The <i>hProcess</i> parameter is ignored. 


### -param lpFlags [out]

A <b>DWORD</b> that receives one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
DEP is disabled for the specified process.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_DEP_ENABLE"></a><a id="process_dep_enable"></a><dl>
<dt><b>PROCESS_DEP_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
DEP is enabled for the specified process.  

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION"></a><a id="process_dep_disable_atl_thunk_emulation"></a><dl>
<dt><b>PROCESS_DEP_DISABLE_ATL_THUNK_EMULATION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
DEP-ATL thunk emulation is disabled for the specified process. For information about DEP-ATL thunk emulation, see <a href="https://msdn.microsoft.com/17c9f522-fd64-4061-9212-8fc91cc96b18">SetProcessDEPPolicy</a>.

</td>
</tr>
</table>
 


### -param lpPermanent [out]

<b>TRUE</b> if DEP is enabled or disabled permanently for the specified process; otherwise <b>FALSE</b>. If <i>lpPermanent</i> is <b>TRUE</b>, the current DEP setting persists for the life of the process and cannot be changed by calling <a href="https://msdn.microsoft.com/17c9f522-fd64-4061-9212-8fc91cc96b18">SetProcessDEPPolicy</a>.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To retrieve error values defined for this function,  call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetProcessDEPPolicy</b> is supported for 32-bit processes only. If this function is called on a 64-bit process, it fails with <b>ERROR_NOT_SUPPORTED</b>.

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/75cd83a5-4b77-4ca9-b595-e32d0dd609d0">Data Execution Prevention</a>



<a href="https://msdn.microsoft.com/82cb1d4e-c0e5-4601-aa55-9171a106c286">GetSystemDEPPolicy</a>



<a href="https://msdn.microsoft.com/17c9f522-fd64-4061-9212-8fc91cc96b18">SetProcessDEPPolicy</a>
 

 

