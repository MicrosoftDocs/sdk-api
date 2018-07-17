---
UID: NF:strmif.IVMRFilterConfig.SetRenderingMode
title: IVMRFilterConfig::SetRenderingMode
author: windows-sdk-content
description: The SetRenderingMode method sets the rendering mode used by the VMR.
old-location: dshow\ivmrfilterconfig_setrenderingmode.htm
old-project: DirectShow
ms.assetid: 11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IVMRFilterConfig interface [DirectShow],SetRenderingMode method, IVMRFilterConfig.SetRenderingMode, IVMRFilterConfig::SetRenderingMode, IVMRFilterConfigSetRenderingMode, SetRenderingMode, SetRenderingMode method [DirectShow], SetRenderingMode method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setrenderingmode, strmif/IVMRFilterConfig::SetRenderingMode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRFilterConfig.SetRenderingMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRFilterConfig::SetRenderingMode


## -description



The <code>SetRenderingMode</code> method sets the rendering mode used by the VMR.




## -parameters




### -param Mode [in]

Specifies the rendering mode as a <a href="https://msdn.microsoft.com/cc924b1a-561f-4d62-8cc8-03ba5e5e8d5b">VMRMode</a> value.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid rendering mode was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The mode cannot be changed for some reason. See Remarks.

</td>
</tr>
</table>
 




## -remarks



The VMR is in <b>VMRMode_Windowed</b> by default. Use this method only if you are putting the VMR into <b>VMRMode_Windowless</b> or <b>VMRMode_Renderless</b> mode. You cannot change the mode after any pin has been connected and you cannot change the mode from windowless or renderless back to windowed, even before any pins are connected. Therefore, specifying <b>VMRMode_Windowed</b> for <i>Mode</i> has no effect under any circumstances.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig Interface</a>



<a href="https://msdn.microsoft.com/139b0326-2ab1-4fa4-91ae-9115b4368660">IVMRFilterConfig::GetRenderingMode</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

