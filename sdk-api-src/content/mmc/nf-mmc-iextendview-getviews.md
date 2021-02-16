---
UID: NF:mmc.IExtendView.GetViews
title: IExtendView::GetViews (mmc.h)
description: The GetViews method retrieves information about the extended view and adds extended views to the result pane.
helpviewer_keywords: ["GetViews","GetViews method [MMC]","GetViews method [MMC]","IExtendView interface","IExtendView interface [MMC]","GetViews method","IExtendView.GetViews","IExtendView::GetViews","_slate_iextendview_getviews","mmc.iextendview_getviews","mmc/IExtendView::GetViews"]
old-location: mmc\iextendview_getviews.htm
tech.root: mmc
ms.assetid: 447b51b1-e206-43c8-8536-049c831dedb7
ms.date: 12/05/2018
ms.keywords: GetViews, GetViews method [MMC], GetViews method [MMC],IExtendView interface, IExtendView interface [MMC],GetViews method, IExtendView.GetViews, IExtendView::GetViews, _slate_iextendview_getviews, mmc.iextendview_getviews, mmc/IExtendView::GetViews
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtendView::GetViews
 - mmc/IExtendView::GetViews
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendView.GetViews
---

# IExtendView::GetViews


## -description

The 
GetViews method retrieves information about the extended view and adds extended views to the result pane.

View extensions use the 
<a href="/windows/desktop/api/mmc/nn-mmc-iviewextensioncallback">IViewExtensionCallback</a> interface methods to provide information about the extended view. A pointer to the 
IViewExtensionCallback interface is provided as a parameter of the <b>IExtendView::GetViews</b> method.

## -parameters

### -param pDataObject [in]

A pointer to the snap-in data object.

### -param pViewExtensionCallback [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/nn-mmc-iviewextensioncallback">IViewExtensionCallback</a> interface. The view extension snap-in uses the 
IViewExtensionCallback interface to add information about the extended view. The snap-in can also call the 
<a href="/windows/desktop/api/mmc/nf-mmc-iviewextensioncallback-addview">IViewExtensionCallback::AddView</a> method multiple times to add multiple extended views. The value in pViewExtensionCallback is valid only during the call to <b>IExtendView::GetViews</b>; view extension snap-ins must not save this pointer for later use.

## -returns

If successful, the return value is S_OK. Other return values indicate an error code.

## -remarks

For more information and a C++ code example for <b>IExtendView::GetViews</b>, see 
<a href="/previous-versions/windows/desktop/mmc/extending-a-primary-snap-ins-view">Extending a Primary Snap-in's View</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/extending-views">Extending Views</a>



<a href="/previous-versions/windows/desktop/mmc/extending-a-primary-snap-ins-view">Extending a Primary Snap-in's View</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iviewextensioncallback">IViewExtensionCallback</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iviewextensioncallback-addview">IViewExtensionCallback::AddView</a>