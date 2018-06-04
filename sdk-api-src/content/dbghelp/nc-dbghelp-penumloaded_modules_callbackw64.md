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

# PENUMLOADED_MODULES_CALLBACKW64 callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/9bfa683f-2a0f-418f-8ac4-5c4224265f2e">EnumerateLoadedModules64</a> function.

The <b>PENUMLOADED_MODULES_CALLBACK64</b> and <b>PENUMLOADED_MODULES_CALLBACKW64</b> types define a pointer to this callback function. 
<i>EnumerateLoadedModulesProc64</i> is a placeholder for the application-defined function name.


## -parameters




### -param ModuleName [in]

The name of the enumerated module.


### -param ModuleBase [in]

The base address of the module. Note that it is possible for this address to become invalid (for example, the module may be unloaded). Use exception handling when accessing the address or passing the address to another function to prevent an access violation from occurring.


### -param ModuleSize [in]

The size of the module, in bytes.


### -param UserContext [in, optional]

Optional user-defined data. This value is passed from 
<a href="https://msdn.microsoft.com/9bfa683f-2a0f-418f-8ac4-5c4224265f2e">EnumerateLoadedModules64</a>.


## -returns



To continue enumeration, the callback function must return <b>TRUE</b>.

To stop enumeration, the callback function must return <b>FALSE</b>.




## -remarks



This callback function supersedes the <i>PENUMLOADED_MODULES_CALLBACK</i> callback function. <i>PENUMLOADED_MODULES_CALLBACK</i> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define PENUMLOADED_MODULES_CALLBACK PENUMLOADED_MODULES_CALLBACK64
#else
typedef BOOL (CALLBACK *PENUMLOADED_MODULES_CALLBACK)(
    __in PCSTR ModuleName,
    __in ULONG ModuleBase,
    __in ULONG ModuleSize,
    __in_opt PVOID UserContext
    );
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/9bfa683f-2a0f-418f-8ac4-5c4224265f2e">EnumerateLoadedModules64</a>
 

 

