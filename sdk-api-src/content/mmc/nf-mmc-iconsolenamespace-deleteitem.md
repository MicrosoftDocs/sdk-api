---
UID: NF:mmc.IConsoleNameSpace.DeleteItem
title: IConsoleNameSpace::DeleteItem (mmc.h)
description: The IConsoleNameSpace2::DeleteItem method IConsoleNameSpaceenables the snap-in to delete a single item from the scope pane.
helpviewer_keywords: ["DeleteItem","DeleteItem method [MMC]","DeleteItem method [MMC]","IConsoleNameSpace interface","DeleteItem method [MMC]","IConsoleNameSpace2 interface","IConsoleNameSpace interface [MMC]","DeleteItem method","IConsoleNameSpace.DeleteItem","IConsoleNameSpace2 interface [MMC]","DeleteItem method","IConsoleNameSpace2::DeleteItem","IConsoleNameSpace::DeleteItem","_slate_iconsolenamespace2_deleteitem","mmc.iconsolenamespace2_deleteitem","mmc/IConsoleNameSpace2::DeleteItem","mmc/IConsoleNameSpace::DeleteItem"]
old-location: mmc\iconsolenamespace2_deleteitem.htm
tech.root: mmc
ms.assetid: 488a6c26-e064-44a1-9842-6f41ec25887c
ms.date: 12/05/2018
ms.keywords: DeleteItem, DeleteItem method [MMC], DeleteItem method [MMC],IConsoleNameSpace interface, DeleteItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],DeleteItem method, IConsoleNameSpace.DeleteItem, IConsoleNameSpace2 interface [MMC],DeleteItem method, IConsoleNameSpace2::DeleteItem, IConsoleNameSpace::DeleteItem, _slate_iconsolenamespace2_deleteitem, mmc.iconsolenamespace2_deleteitem, mmc/IConsoleNameSpace2::DeleteItem, mmc/IConsoleNameSpace::DeleteItem
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
 - IConsoleNameSpace::DeleteItem
 - mmc/IConsoleNameSpace::DeleteItem
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
 - IConsoleNameSpace.DeleteItem
 - IConsoleNameSpace2.DeleteItem
---

# IConsoleNameSpace::DeleteItem


## -description

The <b>IConsoleNameSpace2::DeleteItem</b> method <a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a> enables the snap-in to delete a single item from the scope pane.

## -parameters

### -param hItem [in]

A handle to the item whose child items are to be deleted from the scope pane. If the second argument to <b>IConsoleNameSpace2::DeleteItem</b> is set to <b>TRUE</b>, the item is also deleted.

### -param fDeleteThis [in]

If <b>TRUE</b>, the item specified by hItem is also deleted; otherwise, it is not.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>