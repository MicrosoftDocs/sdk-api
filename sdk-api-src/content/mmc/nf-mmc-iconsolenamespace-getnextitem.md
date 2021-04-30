---
UID: NF:mmc.IConsoleNameSpace.GetNextItem
title: IConsoleNameSpace::GetNextItem (mmc.h)
description: The IConsoleNameSpace2::GetNextItem method enables the snap-in to retrieve the handle to the next item in the scope view.
helpviewer_keywords: ["GetNextItem","GetNextItem method [MMC]","GetNextItem method [MMC]","IConsoleNameSpace interface","GetNextItem method [MMC]","IConsoleNameSpace2 interface","IConsoleNameSpace interface [MMC]","GetNextItem method","IConsoleNameSpace.GetNextItem","IConsoleNameSpace2 interface [MMC]","GetNextItem method","IConsoleNameSpace2::GetNextItem","IConsoleNameSpace::GetNextItem","_slate_iconsolenamespace2_getnextitem","mmc.iconsolenamespace2_getnextitem","mmc/IConsoleNameSpace2::GetNextItem","mmc/IConsoleNameSpace::GetNextItem"]
old-location: mmc\iconsolenamespace2_getnextitem.htm
tech.root: mmc
ms.assetid: 8d512370-bfe5-4a5a-b34b-c1096b6473a3
ms.date: 12/05/2018
ms.keywords: GetNextItem, GetNextItem method [MMC], GetNextItem method [MMC],IConsoleNameSpace interface, GetNextItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],GetNextItem method, IConsoleNameSpace.GetNextItem, IConsoleNameSpace2 interface [MMC],GetNextItem method, IConsoleNameSpace2::GetNextItem, IConsoleNameSpace::GetNextItem, _slate_iconsolenamespace2_getnextitem, mmc.iconsolenamespace2_getnextitem, mmc/IConsoleNameSpace2::GetNextItem, mmc/IConsoleNameSpace::GetNextItem
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
 - IConsoleNameSpace::GetNextItem
 - mmc/IConsoleNameSpace::GetNextItem
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
 - IConsoleNameSpace.GetNextItem
 - IConsoleNameSpace2.GetNextItem
---

# IConsoleNameSpace::GetNextItem


## -description

The <b>IConsoleNameSpace2::GetNextItem</b> method enables the snap-in to retrieve the handle to the next item in the scope view.

## -parameters

### -param item [in]

A handle to an item in the scope pane.

### -param pItemNext [out]

A pointer to the handle to the next item in the scope pane that has been returned.

### -param pCookie [out]

A pointer to the cookie of the next item that has been returned.

## -returns

This method can return one of these values.

## -remarks

If there is no item next to the given item, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>