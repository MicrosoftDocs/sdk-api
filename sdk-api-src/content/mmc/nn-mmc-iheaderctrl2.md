---
UID: NN:mmc.IHeaderCtrl2
title: IHeaderCtrl2 (mmc.h)
description: The IHeaderCtrl2 interface is introduced in MMC 1.2.
helpviewer_keywords: ["IHeaderCtrl2","IHeaderCtrl2 interface [MMC]","IHeaderCtrl2 interface [MMC]","described","_slate_iheaderctrl2","mmc.iheaderctrl2","mmc/IHeaderCtrl2"]
old-location: mmc\iheaderctrl2.htm
tech.root: mmc
ms.assetid: fecf38be-6f45-45ea-a689-ff37b2b92922
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl2, IHeaderCtrl2 interface [MMC], IHeaderCtrl2 interface [MMC],described, _slate_iheaderctrl2, mmc.iheaderctrl2, mmc/IHeaderCtrl2
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHeaderCtrl2
 - mmc/IHeaderCtrl2
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
 - IHeaderCtrl2
---

# IHeaderCtrl2 interface


## -description

The 
<b>IHeaderCtrl2</b> interface is introduced in MMC 1.2.

The 
<b>IHeaderCtrl2</b> interface enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.

<b>IHeaderCtrl2</b> is a new version of the <b>IHeaderCtrl</b> interface for MMC 1.2. 
<b>IHeaderCtrl2</b> is the same as <b>IHeaderCtrl</b> with the addition of the following methods:
<ul>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-setchangetimeout">SetChangeTimeOut</a>
</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-setcolumnfilter">SetColumnFilter</a>
</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-getcolumnfilter">GetColumnFilter</a>
</li>
</ul>These methods provide support for users to filter list views based on filters set on each column in the result view. Be aware that a return value of <b>E_NOTIMPL</b> by any one of these methods indicates that list view filtering is not available in the version of MMC in which the snap-in is loaded.

The 
<b>IHeaderCtrl2</b> interface can be queried from the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole</a> interface passed into 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponent::Initialize</a> during the component's creation.

## -inheritance

The <b>IHeaderCtrl2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHeaderCtrl2</b> also has these types of members:

