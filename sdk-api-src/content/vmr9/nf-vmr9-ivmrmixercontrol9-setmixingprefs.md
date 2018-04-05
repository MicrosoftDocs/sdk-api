---
UID: NF:vmr9.IVMRMixerControl9.SetMixingPrefs
title: IVMRMixerControl9::SetMixingPrefs method
author: windows-driver-content
description: The SetMixingPrefs method sets the mixing preferences for the stream.
old-location: dshow\ivmrmixercontrol9_setmixingprefs.htm
old-project: DirectShow
ms.assetid: db5bf775-685c-4137-846d-fe71cddce08d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IVMRMixerControl9, IVMRMixerControl9 interface [DirectShow], SetMixingPrefs method, IVMRMixerControl9::SetMixingPrefs, IVMRMixerControl9SetMixingPrefs, SetMixingPrefs method [DirectShow], SetMixingPrefs method [DirectShow], IVMRMixerControl9 interface, SetMixingPrefs,IVMRMixerControl9.SetMixingPrefs, dshow.ivmrmixercontrol9_setmixingprefs, vmr9/IVMRMixerControl9::SetMixingPrefs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRMixerControl9.SetMixingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMixerControl9::SetMixingPrefs method


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
 

 

