---
UID: NF:mmc.IComponent.GetDisplayInfo
title: IComponent::GetDisplayInfo (mmc.h)
description: The IComponent::GetDisplayInfo method retrieves display information for an item in the result pane.
helpviewer_keywords: ["GetDisplayInfo","GetDisplayInfo method [MMC]","GetDisplayInfo method [MMC]","IComponent interface","IComponent interface [MMC]","GetDisplayInfo method","IComponent.GetDisplayInfo","IComponent::GetDisplayInfo","_slate_icomponent_getdisplayinfo","mmc.icomponent_getdisplayinfo","mmc/IComponent::GetDisplayInfo"]
old-location: mmc\icomponent_getdisplayinfo.htm
tech.root: mmc
ms.assetid: 8143d11c-3740-4ffc-88f0-6df779c50521
ms.date: 12/05/2018
ms.keywords: GetDisplayInfo, GetDisplayInfo method [MMC], GetDisplayInfo method [MMC],IComponent interface, IComponent interface [MMC],GetDisplayInfo method, IComponent.GetDisplayInfo, IComponent::GetDisplayInfo, _slate_icomponent_getdisplayinfo, mmc.icomponent_getdisplayinfo, mmc/IComponent::GetDisplayInfo
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
 - IComponent::GetDisplayInfo
 - mmc/IComponent::GetDisplayInfo
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
 - IComponent.GetDisplayInfo
---

# IComponent::GetDisplayInfo


## -description

The <b>IComponent::GetDisplayInfo</b> method retrieves display information for an item in the result pane.

## -parameters

### -param pResultDataItem [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure. On input, the mask member specifies the type of data required and the lParam member identifies the item of interest. When called for a virtual list, the nIndex member identifies the desired virtual item and the lParam member is zero.

## -returns

This method can return one of these values.

## -remarks

For virtual lists, MMC calls the 
GetDisplayInfo method only for items that are currently visible in the result pane. This means that 
GetDisplayInfo does not get called for an item until it appears in the result pane.

It is safe to reallocate the memory allocated for members of pResultDataItem only in the following situations:

<ul>
<li>The item is deleted.</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">IComponent::Destroy</a> is called.</li>
<li>GetDisplayInfo is called again for that item.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>