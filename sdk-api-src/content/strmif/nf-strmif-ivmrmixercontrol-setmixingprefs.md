---
UID: NF:strmif.IVMRMixerControl.SetMixingPrefs
title: IVMRMixerControl::SetMixingPrefs
author: windows-sdk-content
description: Sets the mixing preferences for the stream.
old-location: dshow\ivmrmixercontrol_setmixingprefs.htm
tech.root: DirectShow
ms.assetid: b0bd2086-af22-4530-921d-b7c56471d142
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVMRMixerControl interface [DirectShow],SetMixingPrefs method, IVMRMixerControl.SetMixingPrefs, IVMRMixerControl::SetMixingPrefs, IVMRMixerControlSetOutputRect, SetMixingPrefs, SetMixingPrefs method [DirectShow], SetMixingPrefs method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setmixingprefs, strmif/IVMRMixerControl::SetMixingPrefs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl.SetMixingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerControl::SetMixingPrefs


## -description



Sets the mixing preferences for the stream.




## -parameters




### -param dwMixerPrefs [in]

Bitwise <b>OR</b> combination of <a href="https://msdn.microsoft.com/0852590c-6bca-4261-99c0-fff8a012f18e">VMRMixerPrefs</a> flags.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The flags for the mixing preferences are divided into three groups: decimation, filtering, and render target. The VMRMixerPrefs enumeration defines bitmasks to isolate these flags:

<ul>
<li>MixerPref_DecimateMask</li>
<li>MixerPref_FilteringMask</li>
<li>MixerPref_RenderTargetMask</li>
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




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

