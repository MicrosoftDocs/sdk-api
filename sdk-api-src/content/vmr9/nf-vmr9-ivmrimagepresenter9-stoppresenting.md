---
UID: NF:vmr9.IVMRImagePresenter9.StopPresenting
title: IVMRImagePresenter9::StopPresenting (vmr9.h)
author: windows-sdk-content
description: The StopPresenting method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.
old-location: dshow\ivmrimagepresenter9_stoppresenting.htm
tech.root: DirectShow
ms.assetid: 47f34048-3b07-464e-a1f2-f0b49fe76659
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRImagePresenter9 interface [DirectShow],StopPresenting method, IVMRImagePresenter9.StopPresenting, IVMRImagePresenter9::StopPresenting, IVMRImagePresenter9StopPresenting, StopPresenting, StopPresenting method [DirectShow], StopPresenting method [DirectShow],IVMRImagePresenter9 interface, dshow.ivmrimagepresenter9_stoppresenting, vmr9/IVMRImagePresenter9::StopPresenting
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
 - IVMRImagePresenter9.StopPresenting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenter9::StopPresenting


## -description



The <code>StopPresenting</code> method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.




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



<code>StopPresenting</code> can be called only when the VMR is in a running state.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd377391(v=VS.85).aspx">IVMRImagePresenter9 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377393(v=VS.85).aspx">StartPresenting</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

