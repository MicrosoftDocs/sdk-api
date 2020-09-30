---
UID: NF:mmc.IComponentData.GetDisplayInfo
title: IComponentData::GetDisplayInfo (mmc.h)
description: The IComponentData::GetDisplayInfo method retrieves display information for a scope item.
helpviewer_keywords: ["GetDisplayInfo","GetDisplayInfo method [MMC]","GetDisplayInfo method [MMC]","IComponentData interface","IComponentData interface [MMC]","GetDisplayInfo method","IComponentData.GetDisplayInfo","IComponentData::GetDisplayInfo","_slate_icomponentdata_getdisplayinfo","mmc.icomponentdata_getdisplayinfo","mmc/IComponentData::GetDisplayInfo"]
old-location: mmc\icomponentdata_getdisplayinfo.htm
tech.root: mmc
ms.assetid: bd34652a-8e57-44b4-bbc2-99ffadf2a6cf
ms.date: 12/05/2018
ms.keywords: GetDisplayInfo, GetDisplayInfo method [MMC], GetDisplayInfo method [MMC],IComponentData interface, IComponentData interface [MMC],GetDisplayInfo method, IComponentData.GetDisplayInfo, IComponentData::GetDisplayInfo, _slate_icomponentdata_getdisplayinfo, mmc.icomponentdata_getdisplayinfo, mmc/IComponentData::GetDisplayInfo
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
 - IComponentData::GetDisplayInfo
 - mmc/IComponentData::GetDisplayInfo
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
 - IComponentData.GetDisplayInfo
---

# IComponentData::GetDisplayInfo


## -description

The <b>IComponentData::GetDisplayInfo</b> method retrieves display information for a scope item.

## -parameters

### -param pScopeDataItem [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-scopedataitem">SCOPEDATAITEM</a> structure. On input, the structure mask member specifies the type of information required and the lParam member identifies the item of interest.

## -returns

This method can return one of these values.

## -remarks

It is safe to reallocate the memory allocated for members of the pScopeDataItem parameter only:

<ul>
<li>When the scope item is deleted.</li>
<li>When 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-destroy">IComponentData::Destroy</a> is called.</li>
<li>When 
GetDisplayInfo is called again for that scope item.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>