---
UID: NF:mmc.IHeaderCtrl2.SetChangeTimeOut
title: IHeaderCtrl2::SetChangeTimeOut (mmc.h)
description: The IHeaderCtrl2::SetChangeTimeOut sets the time-out interval between the time a change takes place in the filter attributes and the posting of an MMCN_FILTER_CHANGE filter change notification, which is sent to the snap-in's IComponent::Notify method.
helpviewer_keywords: ["IHeaderCtrl2 interface [MMC]","SetChangeTimeOut method","IHeaderCtrl2.SetChangeTimeOut","IHeaderCtrl2::SetChangeTimeOut","SetChangeTimeOut","SetChangeTimeOut method [MMC]","SetChangeTimeOut method [MMC]","IHeaderCtrl2 interface","_slate_iheaderctrl2_setchangetimeout","mmc.iheaderctrl2_setchangetimeout","mmc/IHeaderCtrl2::SetChangeTimeOut"]
old-location: mmc\iheaderctrl2_setchangetimeout.htm
tech.root: mmc
ms.assetid: 26a6a9bc-6556-4576-a810-d7c07c07cfd1
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl2 interface [MMC],SetChangeTimeOut method, IHeaderCtrl2.SetChangeTimeOut, IHeaderCtrl2::SetChangeTimeOut, SetChangeTimeOut, SetChangeTimeOut method [MMC], SetChangeTimeOut method [MMC],IHeaderCtrl2 interface, _slate_iheaderctrl2_setchangetimeout, mmc.iheaderctrl2_setchangetimeout, mmc/IHeaderCtrl2::SetChangeTimeOut
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
 - IHeaderCtrl2::SetChangeTimeOut
 - mmc/IHeaderCtrl2::SetChangeTimeOut
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
 - IHeaderCtrl2.SetChangeTimeOut
---

# IHeaderCtrl2::SetChangeTimeOut


## -description

The <b>IHeaderCtrl2::SetChangeTimeOut</b> sets the time-out interval between the time a change takes place in the filter attributes and the posting of an 
<a href="/previous-versions/windows/desktop/mmc/mmcn-filter-change">MMCN_FILTER_CHANGE</a> filter change notification, which is sent to the snap-in's 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> method.

## -parameters

### -param uTimeout [in]

Filter change interval in milliseconds. The default is an implementation detail of the header control, and as a result MMC does not know about it.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iheaderctrl2">IHeaderCtrl2</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-filter-change">MMCN_FILTER_CHANGE</a>