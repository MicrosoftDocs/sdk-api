---
UID: NF:mmc.IConsoleNameSpace.GetParentItem
title: IConsoleNameSpace::GetParentItem (mmc.h)
description: The IConsoleNameSpace2::GetParentItem method enables the snap-in to retrieve the handle to a parent item in the scope view.
helpviewer_keywords: ["GetParentItem","GetParentItem method [MMC]","GetParentItem method [MMC]","IConsoleNameSpace interface","GetParentItem method [MMC]","IConsoleNameSpace2 interface","IConsoleNameSpace interface [MMC]","GetParentItem method","IConsoleNameSpace.GetParentItem","IConsoleNameSpace2 interface [MMC]","GetParentItem method","IConsoleNameSpace2::GetParentItem","IConsoleNameSpace::GetParentItem","_slate_iconsolenamespace2_getparentitem","mmc.iconsolenamespace2_getparentitem","mmc/IConsoleNameSpace2::GetParentItem","mmc/IConsoleNameSpace::GetParentItem"]
old-location: mmc\iconsolenamespace2_getparentitem.htm
tech.root: mmc
ms.assetid: c4534440-9fbe-41f1-bdf3-767c931a241b
ms.date: 12/05/2018
ms.keywords: GetParentItem, GetParentItem method [MMC], GetParentItem method [MMC],IConsoleNameSpace interface, GetParentItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],GetParentItem method, IConsoleNameSpace.GetParentItem, IConsoleNameSpace2 interface [MMC],GetParentItem method, IConsoleNameSpace2::GetParentItem, IConsoleNameSpace::GetParentItem, _slate_iconsolenamespace2_getparentitem, mmc.iconsolenamespace2_getparentitem, mmc/IConsoleNameSpace2::GetParentItem, mmc/IConsoleNameSpace::GetParentItem
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
 - IConsoleNameSpace::GetParentItem
 - mmc/IConsoleNameSpace::GetParentItem
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
 - IConsoleNameSpace.GetParentItem
 - IConsoleNameSpace2.GetParentItem
---

# IConsoleNameSpace::GetParentItem


## -description

The <b>IConsoleNameSpace2::GetParentItem</b> method enables the snap-in to retrieve the handle to a parent item in the scope view.

## -parameters

### -param item [in]

A handle to an item in the scope pane.

### -param pItemParent [out]

A pointer to the handle to the parent item that is returned.

### -param pCookie [out]

A pointer to the cookie associated with the parent item that is returned.

## -returns

This method can return one of these values.

## -remarks

If the given item has no parent, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>