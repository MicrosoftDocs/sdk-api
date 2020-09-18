---
UID: NF:mmc.IConsoleNameSpace.GetItem
title: IConsoleNameSpace::GetItem (mmc.h)
description: The IConsoleNameSpace2::GetItem method enables the snap-in to retrieve some or all of a single scope item's attributes.
helpviewer_keywords: ["GetItem","GetItem method [MMC]","GetItem method [MMC]","IConsoleNameSpace interface","GetItem method [MMC]","IConsoleNameSpace2 interface","IConsoleNameSpace interface [MMC]","GetItem method","IConsoleNameSpace.GetItem","IConsoleNameSpace2 interface [MMC]","GetItem method","IConsoleNameSpace2::GetItem","IConsoleNameSpace::GetItem","_slate_iconsolenamespace2_getitem","mmc.iconsolenamespace2_getitem","mmc/IConsoleNameSpace2::GetItem","mmc/IConsoleNameSpace::GetItem"]
old-location: mmc\iconsolenamespace2_getitem.htm
tech.root: mmc
ms.assetid: 0dadf9f0-4d49-49c3-a190-dfab0d6ace3f
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [MMC], GetItem method [MMC],IConsoleNameSpace interface, GetItem method [MMC],IConsoleNameSpace2 interface, IConsoleNameSpace interface [MMC],GetItem method, IConsoleNameSpace.GetItem, IConsoleNameSpace2 interface [MMC],GetItem method, IConsoleNameSpace2::GetItem, IConsoleNameSpace::GetItem, _slate_iconsolenamespace2_getitem, mmc.iconsolenamespace2_getitem, mmc/IConsoleNameSpace2::GetItem, mmc/IConsoleNameSpace::GetItem
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
 - IConsoleNameSpace::GetItem
 - mmc/IConsoleNameSpace::GetItem
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
 - IConsoleNameSpace.GetItem
 - IConsoleNameSpace2.GetItem
---

# IConsoleNameSpace::GetItem


## -description

The <b>IConsoleNameSpace2::GetItem</b> method enables the snap-in to retrieve some or all of a single scope item's attributes.

## -parameters

### -param item [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-scopedataitem">SCOPEDATAITEM</a> structure that specifies the information to retrieve and receives information about the item. When the message is sent, the 
ID member of the structure identifies the item and the mask member specifies the attributes to retrieve.

If mask specifies the <b>SDI_STATE</b> value, the <b>nState</b> member contains the item's state information.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace">IConsoleNameSpace</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>