---
UID: NN:mmc.IExtendView
title: IExtendView (mmc.h)
description: The IExtendView interface provides information about the extended view.
old-location: mmc\iextendview.htm
tech.root: mmc
ms.assetid: a6ea8735-4cad-4c04-be97-dfad01b00388
ms.date: 12/05/2018
ms.keywords: IExtendView, IExtendView interface [MMC], IExtendView interface [MMC],described, _slate_iextendview, mmc.iextendview, mmc/IExtendView
ms.topic: interface
f1_keywords:
- mmc/IExtendView
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmc.h
api_name:
- IExtendView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendView interface


## -description


The 
<b>IExtendView</b> interface provides information about the extended view.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendView</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtendView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendview-getviews">GetViews</a>
</td>
<td align="left" width="63%">
Returns the extended view information. MMC calls this method so that a view extension snap-in can add extended views to the result pane.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iextendview">IExtendView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iviewextensioncallback">IViewExtensionCallback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/view-extension-mechanism">View Extension Mechanism</a>
 

 

