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

# WbioQueryEngineInterface function


## -description


Retrieves a pointer to the <a href="https://msdn.microsoft.com/04429f64-ae41-4c26-a777-bdb7aa92b685">WINBIO_ENGINE_INTERFACE</a> structure for the engine adapter.


## -parameters




### -param EngineInterface [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/04429f64-ae41-4c26-a777-bdb7aa92b685">WINBIO_ENGINE_INTERFACE</a> structure.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>EngineInterface</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The Windows Biometric Framework calls this function after loading an engine adapter DLL into memory.
Every engine adapter DLL must therefore implement and export the <b>WbioQueryEngineInterface</b>  function. The function name is case-sensitive, and its spelling and signature must exactly match that  provided in the Syntax section.

To be visible to the Windows Biometric Framework, the <b>WbioQueryEngineInterface</b> function must be named in the EXPORTS section of the export definition linker command file for the DLL.



#### Examples

The following pseudocode shows one possible implementation of this function. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT
WINAPI
WbioQueryEngineInterface(
    __out PWINBIO_ENGINE_INTERFACE *EngineInterface)
{
    // g_EngineInterface is a global variable.
    *EngineInterface = &amp;g_EngineInterface;
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

