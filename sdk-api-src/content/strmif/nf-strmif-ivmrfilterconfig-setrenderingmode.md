---
UID: NF:strmif.IVMRFilterConfig.SetRenderingMode
title: IVMRFilterConfig::SetRenderingMode (strmif.h)
description: The SetRenderingMode method sets the rendering mode used by the VMR.
helpviewer_keywords: ["IVMRFilterConfig interface [DirectShow]","SetRenderingMode method","IVMRFilterConfig.SetRenderingMode","IVMRFilterConfig::SetRenderingMode","IVMRFilterConfigSetRenderingMode","SetRenderingMode","SetRenderingMode method [DirectShow]","SetRenderingMode method [DirectShow]","IVMRFilterConfig interface","dshow.ivmrfilterconfig_setrenderingmode","strmif/IVMRFilterConfig::SetRenderingMode"]
old-location: dshow\ivmrfilterconfig_setrenderingmode.htm
tech.root: dshow
ms.assetid: 11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467
ms.date: 12/05/2018
ms.keywords: IVMRFilterConfig interface [DirectShow],SetRenderingMode method, IVMRFilterConfig.SetRenderingMode, IVMRFilterConfig::SetRenderingMode, IVMRFilterConfigSetRenderingMode, SetRenderingMode, SetRenderingMode method [DirectShow], SetRenderingMode method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setrenderingmode, strmif/IVMRFilterConfig::SetRenderingMode
f1_keywords:
- strmif/IVMRFilterConfig.SetRenderingMode
dev_langs:
- c++
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
- IVMRFilterConfig.SetRenderingMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRFilterConfig::SetRenderingMode


## -description



The <code>SetRenderingMode</code> method sets the rendering mode used by the VMR.




## -parameters




### -param Mode [in]

Specifies the rendering mode as a <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-vmrmode">VMRMode</a> value.


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getrenderingmode">IVMRFilterConfig::GetRenderingMode</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

