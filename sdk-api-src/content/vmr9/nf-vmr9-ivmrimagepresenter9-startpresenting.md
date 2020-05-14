---
UID: NF:vmr9.IVMRImagePresenter9.StartPresenting
title: IVMRImagePresenter9::StartPresenting (vmr9.h)
description: The StartPresenting method is called just before the video starts playing. The allocator-presenter should perform any necessary configuration in this method.helpviewer_keywords: ["IVMRImagePresenter9 interface [DirectShow]","StartPresenting method","IVMRImagePresenter9.StartPresenting","IVMRImagePresenter9::StartPresenting","IVMRImagePresenter9StartPresenting","StartPresenting","StartPresenting method [DirectShow]","StartPresenting method [DirectShow]","IVMRImagePresenter9 interface","dshow.ivmrimagepresenter9_startpresenting","vmr9/IVMRImagePresenter9::StartPresenting"]
old-location: dshow\ivmrimagepresenter9_startpresenting.htm
tech.root: DirectShow
ms.assetid: 654ac7eb-d6ea-4b9a-8dfb-7ba7bc7e8429
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenter9 interface [DirectShow],StartPresenting method, IVMRImagePresenter9.StartPresenting, IVMRImagePresenter9::StartPresenting, IVMRImagePresenter9StartPresenting, StartPresenting, StartPresenting method [DirectShow], StartPresenting method [DirectShow],IVMRImagePresenter9 interface, dshow.ivmrimagepresenter9_startpresenting, vmr9/IVMRImagePresenter9::StartPresenting
f1_keywords:
- vmr9/IVMRImagePresenter9.StartPresenting
dev_langs:
- c++
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
- IVMRImagePresenter9.StartPresenting
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRImagePresenter9::StartPresenting


## -description



The <code>StartPresenting</code> method is called just before the video starts playing. The allocator-presenter should perform any necessary configuration in this method.




## -parameters




### -param dwUserID [in]

An application-defined <b>DWORD_PTR</b> cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.


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



<b>PresentImage</b> can be called when the filter is in either a running or a paused state. <code>StartPresenting</code> and <b>StopPresenting</b> can be called only in a running state. Therefore, if the graph is paused before it is run, <b>PresentImage</b> will be called before <code>StartPresenting</code>.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrimagepresenter9">IVMRImagePresenter9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrimagepresenter9-stoppresenting">StopPresenting</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

