---
UID: NF:mmc.IConsole.UpdateAllViews
title: IConsole::UpdateAllViews (mmc.h)
description: Called by a snap-in when there is a content change in the result pane. This method can be called either by IComponent or IComponentData.
helpviewer_keywords: ["IConsole interface [MMC]","UpdateAllViews method","IConsole.UpdateAllViews","IConsole::UpdateAllViews","UpdateAllViews","UpdateAllViews method [MMC]","UpdateAllViews method [MMC]","IConsole interface","mmc.iconsole_updateallviews","mmc/IConsole::UpdateAllViews"]
old-location: mmc\iconsole_updateallviews.htm
tech.root: mmc
ms.assetid: 72A0FFF3-4084-4AD0-94E4-A7EB03F40BF2
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],UpdateAllViews method, IConsole.UpdateAllViews, IConsole::UpdateAllViews, UpdateAllViews, UpdateAllViews method [MMC], UpdateAllViews method [MMC],IConsole interface, mmc.iconsole_updateallviews, mmc/IConsole::UpdateAllViews
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
 - IConsole::UpdateAllViews
 - mmc/IConsole::UpdateAllViews
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
 - IConsole.UpdateAllViews
---

# IConsole::UpdateAllViews


## -description

Called by a snap-in when there is a content change in the result pane. This method can be called either by 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> or 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>.

## -parameters

### -param lpDataObject [in]

A pointer to a user-supplied data object.

### -param data [in]

A user-defined value, for example a pointer to the modified content.

### -param hint [in]

A user-defined value, for example information about the type of content change.

## -returns

This method can return one of these values.

## -remarks

This method sends an <a href="/previous-versions/windows/desktop/mmc/mmcn-view-change">MMCN_VIEW_CHANGE</a> notification to all instances of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> associated with the snap-in instance calling this method. The <i>lpDataObject</i>, <i>data</i>, and <i>hint</i> parameters are passed as the <i>lpDataObject</i> arg, and param for the 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> method.

This method should be called from the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a> interface pointer obtained through the snap-in 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> implementation.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>



<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>