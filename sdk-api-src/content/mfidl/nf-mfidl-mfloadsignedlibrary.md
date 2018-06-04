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

# MFLoadSignedLibrary function


## -description


Loads a dynamic link library that is signed for the protected environment.


## -parameters




### -param pszName [in]

The name of the dynamic link library to load.  This dynamic link library must be signed for the protected environment.


### -param ppLib [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a> interface for the library.


## -remarks



A singlemodule load count is maintained on the dynamic link library (as it is with <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>).  This load count  is freed when the final release is called on the <a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a> object.


#### Examples

The following example demonstrates how to load a signed library and retrieve the address of a function in that library. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IMFSignedLibrary *pLib;
hr = MFLoadSignedLibrary(TEST_PELOAD_FILE, &amp;pLib);
if (SUCCEEDED(hr))
{
    PVOID functionAddress;
    hr = pLib-&gt;GetProcedureAddress("myFunctionName", &amp;functionAddress);
}
//  Unload the library
pLib-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d32678b0-422d-4fe8-9bbc-fc203a39fdd5">GetProcedureAddress</a>



<a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

