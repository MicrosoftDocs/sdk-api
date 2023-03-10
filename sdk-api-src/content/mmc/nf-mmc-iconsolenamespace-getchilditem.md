---
UID: NF:mmc.IConsoleNameSpace.GetChildItem
title: IConsoleNameSpace::GetChildItem (mmc.h)
description: The IConsoleNameSpace2::GetChildItem method enables the snap-in to get the handle to a child item in the scope pane.
helpviewer_keywords: ["GetChildItem","GetChildItem method [MMC]","GetChildItem method [MMC]","IConsoleNameSpace interface","GetChildItem method [MMC]","IConsoleNameSpace2 interface","IConsoleNameSpace interface [MMC]","GetChildItem method","IConsoleNameSpace.GetChildItem","IConsoleNameSpace2 interface [MMC]","GetChildItem method","IConsoleNameSpace2::GetChildItem","IConsoleNameSpace::GetChildItem","_slate_iconsolenamespace2_getchilditem","mmc.iconsolenamespace2_getchilditem","mmc/IConsoleNameSpace2::GetChildItem","mmc/IConsoleNameSpace::GetChildItem"]
old-location: mmc\iconsolenamespace2_getchilditem.htm
tech.root: mmc
ms.assetid: a320f42e-1dca-4dd9-a919-c4451a48d105
ms.date: 12/05/2018
ms.keywords: GetChildItem, GetChildItem method [MMC], GetChildItem method [MMC],IConsoleNameSpace interface, GetChildItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],GetChildItem method, IConsoleNameSpace.GetChildItem, IConsoleNameSpace2 interface [MMC],GetChildItem method, IConsoleNameSpace2::GetChildItem, IConsoleNameSpace::GetChildItem, _slate_iconsolenamespace2_getchilditem, mmc.iconsolenamespace2_getchilditem, mmc/IConsoleNameSpace2::GetChildItem, mmc/IConsoleNameSpace::GetChildItem
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
 - IConsoleNameSpace::GetChildItem
 - mmc/IConsoleNameSpace::GetChildItem
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
 - IConsoleNameSpace.GetChildItem
 - IConsoleNameSpace2.GetChildItem
---

# IConsoleNameSpace::GetChildItem


## -description

The <b>IConsoleNameSpace2::GetChildItem</b> method enables the snap-in to get the handle to a child item in the scope pane.

## -parameters

### -param item [in]

A handle to a parent item in the scope pane.

### -param pItemChild [out]

A pointer to the handle that identifies the child item in the scope pane that has been returned.

### -param pCookie [out]

A pointer to the cookie associated with the child item that has been returned.

## -returns

This method can return one of these values.

## -remarks

If the handle to the child item is not obtained, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>