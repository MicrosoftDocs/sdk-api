---
UID: NN:strmif.IVMRImagePresenter
title: IVMRImagePresenter (strmif.h)
author: windows-sdk-content
description: The IVMRImagePresenter interface is implemented by the default Allocator-Presenter for the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrimagepresenter.htm
tech.root: DirectShow
ms.assetid: cb9b1e29-45c3-4208-8343-c2924505a9f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenter, IVMRImagePresenter interface [DirectShow], IVMRImagePresenter interface [DirectShow],described, IVMRImagePresenterInterface, dshow.ivmrimagepresenter, strmif/IVMRImagePresenter
ms.topic: interface
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
 - IVMRImagePresenter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenter interface


## -description



The <code>IVMRImagePresenter</code> interface is implemented by the default Allocator-Presenter for the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in Allocator-Presenter that an application provides for the VMR-7. The VMR-7 uses the methods on this interface to inform the Allocator-Presenter that it should present the video frame contained in the supplied Direct Draw surface. Applications do not use this interface.

For the VMR-9, use the <a href="https://msdn.microsoft.com/2c18cdd6-af97-4db2-80b5-bab4cfa25f7d">IVMRImagePresenter9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImagePresenter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRImagePresenter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImagePresenter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df6bf45d-df92-4655-862c-704a12a62ff9">PresentImage</a>
</td>
<td align="left" width="63%">
Called at precisely the moment this video frame should be presented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b97debae-d792-4c9b-a171-11ef2a73e987">StartPresenting</a>
</td>
<td align="left" width="63%">
Called just before the video starts playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6887c66-56ba-4ee6-a740-73213ac088d5">StopPresenting</a>
</td>
<td align="left" width="63%">
Called just after the video stops playing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

