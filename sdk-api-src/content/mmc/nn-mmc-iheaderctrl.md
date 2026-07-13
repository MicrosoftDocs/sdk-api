---
UID: NN:mmc.IHeaderCtrl
title: IHeaderCtrl (mmc.h)
description: Enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.
helpviewer_keywords: ["IHeaderCtrl","IHeaderCtrl interface [MMC]","IHeaderCtrl interface [MMC]","described","mmc.iheaderctrl","mmc/IHeaderCtrl"]
old-location: mmc\iheaderctrl.htm
tech.root: mmc
ms.assetid: 8F7ACE7E-4B44-448A-A3BB-4563DDC9C34E
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl, IHeaderCtrl interface [MMC], IHeaderCtrl interface [MMC],described, mmc.iheaderctrl, mmc/IHeaderCtrl
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
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
 - IHeaderCtrl
 - mmc/IHeaderCtrl
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
 - IHeaderCtrl
---

# IHeaderCtrl interface


## -description

<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.

These methods provide support for users to filter list views based on filters set on each column in the result view. Be aware that a return value of <b>E_NOTIMPL</b> by any one of these methods indicates that list view filtering is not available in the version of MMC in which the snap-in is loaded.

The 
<b>IHeaderCtrl</b> interface can be queried from the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a> interface passed into 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponent::Initialize</a> during the component's creation.

## -inheritance

The <b>IHeaderCtrl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHeaderCtrl</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>
