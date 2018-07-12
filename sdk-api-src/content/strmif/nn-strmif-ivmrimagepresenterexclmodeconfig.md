---
UID: NN:strmif.IVMRImagePresenterExclModeConfig
title: IVMRImagePresenterExclModeConfig
author: windows-sdk-content
description: The IVMRImagePresenterExclModeConfig interface inherits from IVMRImagePresenterConfig and provides methods for setting and retrieving the renderering preferences on the Exclusive Mode Allocator-Presenter.
old-location: dshow\ivmrimagepresenterexclmodeconfig.htm
old-project: DirectShow
ms.assetid: 67c9675c-c0fd-44f6-bdeb-ac3f73e937cc
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IVMRImagePresenterExclModeConfig, IVMRImagePresenterExclModeConfig interface [DirectShow], IVMRImagePresenterExclModeConfig interface [DirectShow],described, dshow.ivmrimagepresenterexclmodeconfig, strmif/IVMRImagePresenterExclModeConfig
ms.prod: windows
ms.technology: windows-sdk
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
 - IVMRImagePresenterExclModeConfig
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRImagePresenterExclModeConfig interface


## -description



The <code>IVMRImagePresenterExclModeConfig</code> interface inherits from <a href="https://msdn.microsoft.com/cbf0fac4-c976-4c1a-ab3a-75ae0d565544">IVMRImagePresenterConfig</a> and provides methods for setting and retrieving the renderering preferences on the Exclusive Mode Allocator-Presenter. This interface is exposed on the DirectDraw Exclusive Mode Allocator-Presenter object. When applications run in DirectDraw Exclusive Mode, they must create their own DirectDraw object, configure the VMR to use the Exclusive Mode Allocator-Presenter, and use this interface to inform the VMR about the DirectDraw object and the primary surface associated with it. For more information, see <a href="https://msdn.microsoft.com/3ef4f267-4dc2-421b-ade4-6b1efa364733">DirectDraw Exclusive Mode</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRImagePresenterExclModeConfig</b> interface inherits from <a href="https://msdn.microsoft.com/cbf0fac4-c976-4c1a-ab3a-75ae0d565544">IVMRImagePresenterConfig</a>. <b>IVMRImagePresenterExclModeConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/09b756de-7fd2-44d8-9ef3-6b5dc56cb8b3">GetXlcModeDDObjAndPrimarySurface</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw object and primary surface currently being used by a VMR that has been configured for DirectDraw Exclusive Mode using the <b>SetXlcModeDDObjAndPrimarySurface</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af69975-fe3c-45e6-b1f5-ce2dbda9a4dc">SetXlcModeDDObjAndPrimarySurface</a>
</td>
<td align="left" width="63%">
Informs the VMR of the DirectDraw object and primary surface that were created by the application.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cbf0fac4-c976-4c1a-ab3a-75ae0d565544">IVMRImagePresenterConfig</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

