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

# SHCreateDefaultExtractIcon function


## -description


Creates a standard icon extractor, whose defaults can be further configured via the <a href="https://msdn.microsoft.com/27b952e3-f17a-4844-8c39-2ae240179d02">IDefaultExtractIconInit</a> interface.


## -parameters




### -param riid

Type: <b>REFIID</b>

A reference to interface ID.


### -param ppv [out]

Type: <b>void**</b>

The address of <a href="https://msdn.microsoft.com/27b952e3-f17a-4844-8c39-2ae240179d02">IDefaultExtractIconInit</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The intended usage for this function is as follows:
            
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IExtractIcon *pxi;

IDefaultExtractIconInit *pdxi;

HRESULT hr = SHCreateDefaultExtractIcon(IID_PPV_ARGS(&amp;pdxi);

 if (SUCCEEDED(hr)) &amp;&amp;

      SUCCEEDED(hr = pdxi-&gt;SetFlags(GIL_PERCLASS)) &amp;&amp;

      SUCCEEDED(hr = pdxi-&gt;SetKey(hkey)) &amp;&amp;   // optional

      SUCCEEDED(hr = pdxi-&gt;SetNormalIcon(L"this.dll", 1)) &amp;&amp;

      SUCCEEDED(hr = pdxi-&gt;SetOpenIcon(NULL, SIID_FOLDEROPEN)) &amp;&amp; // optional

      SUCCEEDED(hr = pdxi-&gt;SetDefaultIcon(NULL, SIID_FOLDER)) &amp;&amp; // optional

      SUCCEEDED(hr = pdxi-&gt;SetShortcutIcon(L"this.dll", 2))) // optional

{

      hr = pdxi-&gt;QueryInterface(IID_PPV_ARGS(&amp;pxi)) 

}

 if (pdxi)

{

    pdxi-&gt;Release();

}</pre>
</td>
</tr>
</table></span></div>


