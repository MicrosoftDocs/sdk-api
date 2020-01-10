---
UID: NN:mmc.IViewExtensionCallback
title: IViewExtensionCallback (mmc.h)
description: The IViewExtensionCallback interface is used to add a view to the result pane.
old-location: mmc\iviewextensioncallback.htm
tech.root: mmc
ms.assetid: 1854ab01-e518-4ff4-a1d5-d1e03b348992
ms.date: 12/05/2018
ms.keywords: IViewExtensionCallback, IViewExtensionCallback interface [MMC], IViewExtensionCallback interface [MMC],described, _slate_iviewextensioncallback, mmc.iviewextensioncallback, mmc/IViewExtensionCallback
f1_keywords:
- mmc/IViewExtensionCallback
dev_langs:
- c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmcndmgr.dll
api_name:
- IViewExtensionCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IViewExtensionCallback interface


## -description


The 
<b>IViewExtensionCallback</b> interface is used to add a view to the result pane. During the call to the view extension's 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendview-getviews">IExtendView::GetViews</a> method, MMC provides an <b>IViewExtensionCallback</b> interface pointer; this pointer is valid only during the call and should not be saved for later use.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IViewExtensionCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IViewExtensionCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IViewExtensionCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iviewextensioncallback-addview">AddView</a>
</td>
<td align="left" width="63%">
Adds a view to the result pane, and optionally removes the standard view.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/extending-views">Extending Views</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iextendview">IExtendView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendview-getviews">IExtendView::GetViews</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/view-extension-mechanism">View Extension Mechanism</a>
 

 

