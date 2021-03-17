---
UID: NF:mmc.IConsoleNameSpace.SetItem
title: IConsoleNameSpace::SetItem (mmc.h)
description: The IConsoleNameSpace2::SetItem method enables the snap-in to set the attributes of a single scope-view item.
helpviewer_keywords: ["IConsoleNameSpace interface [MMC]","SetItem method","IConsoleNameSpace.SetItem","IConsoleNameSpace2 interface [MMC]","SetItem method","IConsoleNameSpace2::SetItem","IConsoleNameSpace::SetItem","SetItem","SetItem method [MMC]","SetItem method [MMC]","IConsoleNameSpace interface","SetItem method [MMC]","IConsoleNameSpace2 interface","_slate_iconsolenamespace2_setitem","mmc.iconsolenamespace2_setitem","mmc/IConsoleNameSpace2::SetItem","mmc/IConsoleNameSpace::SetItem"]
old-location: mmc\iconsolenamespace2_setitem.htm
tech.root: mmc
ms.assetid: e63dd8dd-dcef-4d52-96f7-cf9a7e42a0f1
ms.date: 12/05/2018
ms.keywords: IConsoleNameSpace interface [MMC],SetItem method, IConsoleNameSpace.SetItem, IConsoleNameSpace2 interface [MMC],SetItem method, IConsoleNameSpace2::SetItem, IConsoleNameSpace::SetItem, SetItem, SetItem method [MMC], SetItem method [MMC],IConsoleNameSpace interface, SetItem method [MMC],IConsoleNameSpace2 interface, _slate_iconsolenamespace2_setitem, mmc.iconsolenamespace2_setitem, mmc/IConsoleNameSpace2::SetItem, mmc/IConsoleNameSpace::SetItem
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
 - IConsoleNameSpace::SetItem
 - mmc/IConsoleNameSpace::SetItem
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
 - IConsoleNameSpace.SetItem
 - IConsoleNameSpace2.SetItem
---

# IConsoleNameSpace::SetItem


## -description

The <b>IConsoleNameSpace2::SetItem</b> method enables the snap-in to set the attributes of a single scope-view item.

## -parameters

### -param item [in]

A pointer to a <a href="/windows/desktop/api/mmc/ns-mmc-scopedataitem">SCOPEDATAITEM</a> structure that contains 
      information about the item to be set in the scope pane.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>