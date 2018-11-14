---
UID: NF:strmif.IVMRFilterConfig.SetImageCompositor
title: IVMRFilterConfig::SetImageCompositor
author: windows-sdk-content
description: The SetImageCompositor method installs an application-provided image compositor.
old-location: dshow\ivmrfilterconfig_setimagecompositor.htm
tech.root: DirectShow
ms.assetid: 504380d4-4df6-4b01-8db3-5c769a3d4106
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRFilterConfig interface [DirectShow],SetImageCompositor method, IVMRFilterConfig.SetImageCompositor, IVMRFilterConfig::SetImageCompositor, IVMRFilterConfigSetImageCompositor, SetImageCompositor, SetImageCompositor method [DirectShow], SetImageCompositor method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setimagecompositor, strmif/IVMRFilterConfig::SetImageCompositor
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
 - IVMRFilterConfig.SetImageCompositor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IVMRFilterConfig.SetImageCompositor
: 
---

# IVMRFilterConfig::SetImageCompositor


## -description



The <code>SetImageCompositor</code> method installs an application-provided image compositor.




## -parameters




### -param lpVMRImgCompositor [in]

Pointer to the image compositor's <a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor</a> interface.


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

The compositor is automatically loaded when the VMR is in windowless or windowed mode. When the VMR is in renderless mode, the compositor must be loaded by calling <a href="https://msdn.microsoft.com/cd200b33-bb74-474a-9047-d81cb470af23">IVMRFilterConfig::SetNumberOfStreams</a>. The VMR manages all reference counting on the <a href="https://msdn.microsoft.com/d905e871-c156-4140-bb3f-a19fa0cd79be">IVMRImageCompositor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

