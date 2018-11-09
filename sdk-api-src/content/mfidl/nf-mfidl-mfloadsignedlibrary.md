---
UID: NF:mfidl.MFLoadSignedLibrary
title: MFLoadSignedLibrary function
author: windows-sdk-content
description: Loads a dynamic link library that is signed for the protected environment.
old-location: mf\mfloadsignedlibrary.htm
tech.root: medfound
ms.assetid: 979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFLoadSignedLibrary, MFLoadSignedLibrary function [Media Foundation], mf.mfloadsignedlibrary, mfidl/MFLoadSignedLibrary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFLoadSignedLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

