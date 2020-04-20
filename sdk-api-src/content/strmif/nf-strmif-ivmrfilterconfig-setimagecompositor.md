---
UID: NF:strmif.IVMRFilterConfig.SetImageCompositor
title: IVMRFilterConfig::SetImageCompositor (strmif.h)
description: The SetImageCompositor method installs an application-provided image compositor.helpviewer_keywords: ["IVMRFilterConfig interface [DirectShow]","SetImageCompositor method","IVMRFilterConfig.SetImageCompositor","IVMRFilterConfig::SetImageCompositor","IVMRFilterConfigSetImageCompositor","SetImageCompositor","SetImageCompositor method [DirectShow]","SetImageCompositor method [DirectShow]","IVMRFilterConfig interface","dshow.ivmrfilterconfig_setimagecompositor","strmif/IVMRFilterConfig::SetImageCompositor"]
old-location: dshow\ivmrfilterconfig_setimagecompositor.htm
tech.root: DirectShow
ms.assetid: 504380d4-4df6-4b01-8db3-5c769a3d4106
ms.date: 12/05/2018
ms.keywords: IVMRFilterConfig interface [DirectShow],SetImageCompositor method, IVMRFilterConfig.SetImageCompositor, IVMRFilterConfig::SetImageCompositor, IVMRFilterConfigSetImageCompositor, SetImageCompositor, SetImageCompositor method [DirectShow], SetImageCompositor method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setimagecompositor, strmif/IVMRFilterConfig::SetImageCompositor
f1_keywords:
- strmif/IVMRFilterConfig.SetImageCompositor
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
- IVMRFilterConfig.SetImageCompositor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRFilterConfig::SetImageCompositor


## -description



The <code>SetImageCompositor</code> method installs an application-provided image compositor.




## -parameters




### -param lpVMRImgCompositor [in]

Pointer to the image compositor's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface.


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
The mixer is not currently loaded.

</td>
</tr>
</table>
 




## -remarks



Use this method to replace the VMR's default compositor with a custom compositor provided by the application. The image compositor is a sub-component of the mixer.

The compositor is automatically loaded when the VMR is in windowless or windowed mode. When the VMR is in renderless mode, the compositor must be loaded by calling <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams">IVMRFilterConfig::SetNumberOfStreams</a>. The VMR manages all reference counting on the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

