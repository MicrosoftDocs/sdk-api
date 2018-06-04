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

# IVMRMixerControl9::SetMixingPrefs


## -description



The <code>SetMixingPrefs</code> method sets the mixing preferences for the stream.




## -parameters




### -param dwMixerPrefs [in]

Bitwise OR combination of <a href="https://msdn.microsoft.com/59d3af89-248e-43cd-b6dc-e6c0a4d5f5fb">VMR9MixerPrefs</a> flags.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The flags for the mixing preferences are divided into three groups: decimation, filtering, and render target. The VMR9MixerPrefs enumeration defines bitmasks to isolate these flags:

<ul>
<li>MixerPref9_DecimateMask</li>
<li>MixerPref9_FilteringMask</li>
<li>MixerPref9_RenderTargetMask</li>
</ul>
You must specify a valid flag for each group. If you want to change a single flag, you can get the current preferences, remove the flag you don't want, and add the flag you want. For example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get the current mixing preferences.
DWORD dwPrefs;
pMixControl-&gt;GetMixingPrefs(&amp;dwPrefs);  

// Remove the current render target flag.
dwPrefs &amp;= ~MixerPref_RenderTargetMask; 

// Add the render target flag that we want.
dwPrefs |= MixerPref_RenderTargetYUV;

// Set the new flags.
pMixControl-&gt;SetMixingPrefs(dwPrefs);
</pre>
</td>
</tr>
</table></span></div>
If the VMR is in renderless mode, you must set the allocator-presenter before calling <code>SetMixingPrefs</code>. Otherwise, the VMR cannot determine the capabilities of the Direct3D device.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/f311303a-8270-40b6-8153-e0bd8b232c69">IVMRMixerControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

