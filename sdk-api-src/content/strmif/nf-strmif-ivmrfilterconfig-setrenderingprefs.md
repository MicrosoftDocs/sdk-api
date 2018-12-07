---
UID: NF:strmif.IVMRFilterConfig.SetRenderingPrefs
title: IVMRFilterConfig::SetRenderingPrefs
author: windows-sdk-content
description: The SetRenderingPrefs method sets various application preferences related to video rendering.
old-location: dshow\ivmrfilterconfig_setrenderingprefs.htm
tech.root: DirectShow
ms.assetid: 1374d071-f396-4fcb-8ca2-ac3986960207
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRFilterConfig interface [DirectShow],SetRenderingPrefs method, IVMRFilterConfig.SetRenderingPrefs, IVMRFilterConfig::SetRenderingPrefs, IVMRFilterConfigSetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setrenderingprefs, strmif/IVMRFilterConfig::SetRenderingPrefs
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
 - IVMRFilterConfig.SetRenderingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRFilterConfig::SetRenderingPrefs


## -description



The <code>SetRenderingPrefs</code> method sets various application preferences related to video rendering.




## -parameters




### -param dwRenderFlags [in]

Double word containing a bitwise OR of <a href="https://msdn.microsoft.com/cfe1d4a7-b1ec-4d8e-b6d5-3fe5a530c352">VMRRenderPrefs</a> values specifying the rendering preferences.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
No allocator-presenter is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwRenderFlags</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



This method calls through to the allocator-presenter's <a href="https://msdn.microsoft.com/22bb6d52-2201-429d-bd1a-d031c9b017ae">IVMRImagePresenterConfig::SetRenderingPrefs</a> method. (The default allocator-presenter exposes <a href="https://msdn.microsoft.com/cbf0fac4-c976-4c1a-ab3a-75ae0d565544">IVMRImagePresenterConfig</a>. Custom allocator-presenters can also expose this interface if desired.) If the VMR-7 has not yet created the default allocator-presenter, or if the application provided a custom allocator-presenter which does not support <b>IVMRImagePresenterConfig</b>, this method returns VFW_E_WRONG_STATE. To create the default allocator-presenter, call <a href="https://msdn.microsoft.com/11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467">IVMRFilterConfig::SetRenderingMode</a> with the value VMRMode_Windowed or VMRMode_Windowed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig Interface</a>



<a href="https://msdn.microsoft.com/aabf3628-3179-430c-a74b-0cb4e552cbe2">IVMRFilterConfig::GetRenderingPrefs</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

