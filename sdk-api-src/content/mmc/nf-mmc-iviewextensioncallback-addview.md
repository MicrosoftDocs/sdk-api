---
UID: NF:mmc.IViewExtensionCallback.AddView
title: IViewExtensionCallback::AddView (mmc.h)
description: Adds a view to the result pane.
helpviewer_keywords: ["AddView","AddView method [MMC]","AddView method [MMC]","IViewExtensionCallback interface","IViewExtensionCallback interface [MMC]","AddView method","IViewExtensionCallback.AddView","IViewExtensionCallback::AddView","_slate_iviewextensioncallback_addview","mmc.iviewextensioncallback_addview","mmc/IViewExtensionCallback::AddView"]
old-location: mmc\iviewextensioncallback_addview.htm
tech.root: mmc
ms.assetid: 3e794787-d328-4cbf-822e-8846fed81a57
ms.date: 12/05/2018
ms.keywords: AddView, AddView method [MMC], AddView method [MMC],IViewExtensionCallback interface, IViewExtensionCallback interface [MMC],AddView method, IViewExtensionCallback.AddView, IViewExtensionCallback::AddView, _slate_iviewextensioncallback_addview, mmc.iviewextensioncallback_addview, mmc/IViewExtensionCallback::AddView
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
 - IViewExtensionCallback::AddView
 - mmc/IViewExtensionCallback::AddView
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
 - IViewExtensionCallback.AddView
---

# IViewExtensionCallback::AddView


## -description

The 
AddView method adds a view to the result pane. This method is implemented by MMC and is called by view extensions. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/extending-views">Extending Views</a>.

## -parameters

### -param pExtViewData [in]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_ext_view_data">MMC_EXT_VIEW_DATA</a> structure, which contains information about the view being added to the result pane. The bReplacesDefaultView member of the 
<b>MMC_EXT_VIEW_DATA</b> structure determines if the standard view is removed when adding the new view.

## -returns

If successful, the return value is S_OK. Other return values indicate an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/extending-views">Extending Views</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendview">IExtendView</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendview-getviews">IExtendView::GetViews</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_ext_view_data">MMC_EXT_VIEW_DATA</a>



<a href="/previous-versions/windows/desktop/mmc/view-extension-mechanism">View Extension Mechanism</a>