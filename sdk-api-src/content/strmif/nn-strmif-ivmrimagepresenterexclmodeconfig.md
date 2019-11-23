---
UID: NN:strmif.IVMRImagePresenterExclModeConfig
title: IVMRImagePresenterExclModeConfig (strmif.h)

description: The IVMRImagePresenterExclModeConfig interface inherits from IVMRImagePresenterConfig and provides methods for setting and retrieving the renderering preferences on the Exclusive Mode Allocator-Presenter.
old-location: dshow\ivmrimagepresenterexclmodeconfig.htm
tech.root: DirectShow
ms.assetid: 67c9675c-c0fd-44f6-bdeb-ac3f73e937cc

ms.date: 12/05/2018
ms.keywords: IVMRImagePresenterExclModeConfig, IVMRImagePresenterExclModeConfig interface [DirectShow], IVMRImagePresenterExclModeConfig interface [DirectShow],described, dshow.ivmrimagepresenterexclmodeconfig, strmif/IVMRImagePresenterExclModeConfig
ms.topic: interface
f1_keywords: 
 - "strmif/IVMRImagePresenterExclModeConfig"
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
 - IVMRImagePresenterExclModeConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRImagePresenterExclModeConfig interface


## -description



The <code>IVMRImagePresenterExclModeConfig</code> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a> and provides methods for setting and retrieving the renderering preferences on the Exclusive Mode Allocator-Presenter. This interface is exposed on the DirectDraw Exclusive Mode Allocator-Presenter object. When applications run in DirectDraw Exclusive Mode, they must create their own DirectDraw object, configure the VMR to use the Exclusive Mode Allocator-Presenter, and use this interface to inform the VMR about the DirectDraw object and the primary surface associated with it. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/directdraw-exclusive-mode">DirectDraw Exclusive Mode</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImagePresenterExclModeConfig</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a>. <b>IVMRImagePresenterExclModeConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRImagePresenterExclModeConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenterexclmodeconfig-getxlcmodeddobjandprimarysurface">GetXlcModeDDObjAndPrimarySurface</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw object and primary surface currently being used by a VMR that has been configured for DirectDraw Exclusive Mode using the <b>SetXlcModeDDObjAndPrimarySurface</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenterexclmodeconfig-setxlcmodeddobjandprimarysurface">SetXlcModeDDObjAndPrimarySurface</a>
</td>
<td align="left" width="63%">
Informs the VMR of the DirectDraw object and primary surface that were created by the application.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

