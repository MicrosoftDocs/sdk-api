---
UID: NF:vmr9.IVMRImagePresenter9.PresentImage
title: IVMRImagePresenter9::PresentImage
author: windows-sdk-content
description: The PresentImage method is called at precisely the moment this video frame should be presented.
old-location: dshow\ivmrimagepresenter9_presentimage.htm
old-project: DirectShow
ms.assetid: 1c642958-88df-48b2-8eb1-0d032af71f71
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IVMRImagePresenter9 interface [DirectShow],PresentImage method, IVMRImagePresenter9.PresentImage, IVMRImagePresenter9::PresentImage, IVMRImagePresenter9PresentImage, PresentImage, PresentImage method [DirectShow], PresentImage method [DirectShow],IVMRImagePresenter9 interface, dshow.ivmrimagepresenter9_presentimage, vmr9/IVMRImagePresenter9::PresentImage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VMR9DeinterlaceTech
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRImagePresenter9.PresentImage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRImagePresenter9::PresentImage


## -description



The <code>PresentImage</code> method is called at precisely the moment this video frame should be presented.




## -parameters




### -param dwUserID [in]

An application-defined DWORD_PTR that uniquely identifies this instance of the VMR in scenarios when multiple instances of the VMR are being used with a single instance of an allocator-presenter. See Remarks.


### -param lpPresInfo [in]

Specifies a <a href="https://msdn.microsoft.com/7e5cf0e9-1cb9-494a-9370-550328dcd85c">VMR9PresentationInfo</a> structure that contains information about the video frame.


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



<code>PresentImage</code> can be called when the filter is in either a running or a paused state. <b>StartPresenting</b> and <b>StopPresenting</b> can be called only in a running state. Therefore, if the graph is paused before it is run, <code>PresentImage</code> will be called before <b>StartPresenting</b>.

Applications can create custom blending effects by using a single instance of an allocator-presenter with multiple instances of the VMR either in a single filter graph or in multiple filter graphs. Using the allocator presenter in this way enables applications to blend streams from different filter graphs, or blend different streams within the same filter graph. If you are using a single instance of the VMR, set this value to zero.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/2c18cdd6-af97-4db2-80b5-bab4cfa25f7d">IVMRImagePresenter9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

