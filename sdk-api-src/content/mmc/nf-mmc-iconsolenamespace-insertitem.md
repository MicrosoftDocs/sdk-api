---
UID: NF:mmc.IConsoleNameSpace.InsertItem
title: IConsoleNameSpace::InsertItem (mmc.h)
description: The IConsoleNameSpace2::InsertItem method enables the snap-in to insert a single item into the scope view.
helpviewer_keywords: ["IConsoleNameSpace interface [MMC]","InsertItem method","IConsoleNameSpace.InsertItem","IConsoleNameSpace2 interface [MMC]","InsertItem method","IConsoleNameSpace2::InsertItem","IConsoleNameSpace::InsertItem","InsertItem","InsertItem method [MMC]","InsertItem method [MMC]","IConsoleNameSpace interface","InsertItem method [MMC]","IConsoleNameSpace2 interface","_slate_iconsolenamespace2_insertitem","mmc.iconsolenamespace2_insertitem","mmc/IConsoleNameSpace2::InsertItem","mmc/IConsoleNameSpace::InsertItem"]
old-location: mmc\iconsolenamespace2_insertitem.htm
tech.root: mmc
ms.assetid: 1966c4d1-acb1-496a-92d2-c0437c95fba6
ms.date: 12/05/2018
ms.keywords: IConsoleNameSpace interface [MMC],InsertItem method, IConsoleNameSpace.InsertItem, IConsoleNameSpace2 interface [MMC],InsertItem method, IConsoleNameSpace2::InsertItem, IConsoleNameSpace::InsertItem, InsertItem, InsertItem method [MMC], InsertItem method [MMC],IConsoleNameSpace interface, InsertItem method [MMC],IConsoleNameSpace2 interface, _slate_iconsolenamespace2_insertitem, mmc.iconsolenamespace2_insertitem, mmc/IConsoleNameSpace2::InsertItem, mmc/IConsoleNameSpace::InsertItem
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
 - IConsoleNameSpace::InsertItem
 - mmc/IConsoleNameSpace::InsertItem
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
 - IConsoleNameSpace.InsertItem
 - IConsoleNameSpace2.InsertItem
---

# IConsoleNameSpace::InsertItem


## -description

The <b>IConsoleNameSpace2::InsertItem</b> method enables the snap-in to insert a single item into the scope view.

## -parameters

### -param item [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-scopedataitem">SCOPEDATAITEM</a> structure that specifies the attributes of the new scope item. On return, the 
ID member of the structure contains the item identifier assigned by MMC for the newly inserted item. Be aware that this value is the <b>HSCOPEITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getitem">IConsoleNameSpace2::GetItem</a>.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>