---
UID: NN:mmc.IViewExtensionCallback
title: IViewExtensionCallback (mmc.h)
description: The IViewExtensionCallback interface is used to add a view to the result pane.
helpviewer_keywords: ["IViewExtensionCallback","IViewExtensionCallback interface [MMC]","IViewExtensionCallback interface [MMC]","described","_slate_iviewextensioncallback","mmc.iviewextensioncallback","mmc/IViewExtensionCallback"]
old-location: mmc\iviewextensioncallback.htm
tech.root: mmc
ms.assetid: 1854ab01-e518-4ff4-a1d5-d1e03b348992
ms.date: 12/05/2018
ms.keywords: IViewExtensionCallback, IViewExtensionCallback interface [MMC], IViewExtensionCallback interface [MMC],described, _slate_iviewextensioncallback, mmc.iviewextensioncallback, mmc/IViewExtensionCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IViewExtensionCallback
 - mmc/IViewExtensionCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IViewExtensionCallback
---

# IViewExtensionCallback interface


## -description

The 
<b>IViewExtensionCallback</b> interface is used to add a view to the result pane. During the call to the view extension's 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendview-getviews">IExtendView::GetViews</a> method, MMC provides an <b>IViewExtensionCallback</b> interface pointer; this pointer is valid only during the call and should not be saved for later use.

## -inheritance

The <b>IViewExtensionCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IViewExtensionCallback</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/mmc/extending-views">Extending Views</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendview">IExtendView</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendview-getviews">IExtendView::GetViews</a>



<a href="/previous-versions/windows/desktop/mmc/view-extension-mechanism">View Extension Mechanism</a>
