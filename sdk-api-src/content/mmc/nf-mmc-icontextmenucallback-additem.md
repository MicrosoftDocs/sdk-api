---
UID: NF:mmc.IContextMenuCallback.AddItem
title: IContextMenuCallback::AddItem (mmc.h)
description: The IContextMenuCallback::AddItem method adds a single item to a context menu.
helpviewer_keywords: ["AddItem","AddItem method [MMC]","AddItem method [MMC]","IContextMenuCallback interface","IContextMenuCallback interface [MMC]","AddItem method","IContextMenuCallback.AddItem","IContextMenuCallback::AddItem","_slate_icontextmenucallback_additem","mmc.icontextmenucallback_additem","mmc/IContextMenuCallback::AddItem"]
old-location: mmc\icontextmenucallback_additem.htm
tech.root: mmc
ms.assetid: 7186f201-13aa-4357-9b89-b435d244229c
ms.date: 12/05/2018
ms.keywords: AddItem, AddItem method [MMC], AddItem method [MMC],IContextMenuCallback interface, IContextMenuCallback interface [MMC],AddItem method, IContextMenuCallback.AddItem, IContextMenuCallback::AddItem, _slate_icontextmenucallback_additem, mmc.icontextmenucallback_additem, mmc/IContextMenuCallback::AddItem
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
 - IContextMenuCallback::AddItem
 - mmc/IContextMenuCallback::AddItem
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
 - IContextMenuCallback.AddItem
---

# IContextMenuCallback::AddItem


## -description

The <b>IContextMenuCallback::AddItem</b> method adds a single item to a context menu.

## -parameters

### -param pItem [in]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-contextmenuitem">CONTEXTMENUITEM</a> structure with the item to be added. This parameter cannot be <b>NULL</b>.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/ns-mmc-contextmenuitem">CONTEXTMENUITEM</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenucallback">IContextMenuCallback</a>