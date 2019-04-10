---
UID: NN:strmif.IVMRImagePresenterConfig
title: IVMRImagePresenterConfig (strmif.h)
author: windows-sdk-content
description: The IVMRImagePresenterConfig interface provides methods for setting the renderering preferences on the allocator-presenter used by the Video Mixing Renderer Filter 7 (VMR-7).Applications should not use this interface directly.
old-location: dshow\ivmrimagepresenterconfig.htm
tech.root: DirectShow
ms.assetid: cbf0fac4-c976-4c1a-ab3a-75ae0d565544
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenterConfig, IVMRImagePresenterConfig interface [DirectShow], IVMRImagePresenterConfig interface [DirectShow],described, IVMRImagePresenterConfigInterface, dshow.ivmrimagepresenterconfig, strmif/IVMRImagePresenterConfig
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
 - IVMRImagePresenterConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenterConfig interface


## -description



The <code>IVMRImagePresenterConfig</code> interface provides methods for setting the renderering preferences on the allocator-presenter used by the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7).

Applications should not use this interface directly. The VMR-7 filter's <b>IVMRFilterConfig</b> interface calls methods on this interface. The default allocator-presenter implements this interface. Custom allocator-presenters can also expose this interface.

For the VMR-9, use the <a href="https://msdn.microsoft.com/fc3c9b4d-0213-47d5-96e4-db582c80ca4e">IVMRImagePresenterConfig9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImagePresenterConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRImagePresenterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImagePresenterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ca9c02-e38d-4600-aee8-08afd03423ad">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Gets the rendering preferences.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22bb6d52-2201-429d-bd1a-d031c9b017ae">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets the rendering preferences.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

