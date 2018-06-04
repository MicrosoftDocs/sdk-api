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

# D3D12GetDebugInterface function


## -description



          Gets a debug interface.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


            The globally unique identifier (<b>GUID</b>) for the debug interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the debug interface can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="https://msdn.microsoft.com/6CFAE096-EE09-4DD0-ADA3-A700FD9FDCB9">ID3D12Debug</a>) will get the <b>GUID</b> of the debug interface.
          


### -param ppvDebug [out, optional]

Type: <b>void**</b>


            The debug interface, as a pointer to pointer to void.
            See
            <a href="https://msdn.microsoft.com/6CFAE096-EE09-4DD0-ADA3-A700FD9FDCB9">ID3D12Debug</a>
            and
            <a href="https://msdn.microsoft.com/6FD77F14-E260-4DBB-8434-664DE1F6DE39">ID3D12DebugDevice</a>.
            


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




        The function signature PFN_D3D12_GET_DEBUG_INTERFACE is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      


#### Examples

Enable the D3D12 debug layer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Enable the D3D12 debug layer.
{
    
    ComPtr&lt;ID3D12Debug&gt; debugController;
    if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&amp;debugController))))
    {
        debugController-&gt;EnableDebugLayer();
    }
}
</pre>
</td>
</tr>
</table></span></div>

            Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/C0F9A52C-483D-40B2-9E1F-CB92ADDC2856">Core Functions</a>
 

 

