---
UID: NF:mmc.IResultOwnerData.FindItem
title: IResultOwnerData::FindItem (mmc.h)
description: Finds the next item in a virtual list matching a specified string.
helpviewer_keywords: ["FindItem","FindItem method [MMC]","FindItem method [MMC]","IResultOwnerData interface","IResultOwnerData interface [MMC]","FindItem method","IResultOwnerData.FindItem","IResultOwnerData::FindItem","_slate_iresultownerdata_finditem","mmc.iresultownerdata_finditem","mmc/IResultOwnerData::FindItem"]
old-location: mmc\iresultownerdata_finditem.htm
tech.root: mmc
ms.assetid: 839e6038-3f47-4192-b717-d81e4d9f202d
ms.date: 12/05/2018
ms.keywords: FindItem, FindItem method [MMC], FindItem method [MMC],IResultOwnerData interface, IResultOwnerData interface [MMC],FindItem method, IResultOwnerData.FindItem, IResultOwnerData::FindItem, _slate_iresultownerdata_finditem, mmc.iresultownerdata_finditem, mmc/IResultOwnerData::FindItem
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
 - IResultOwnerData::FindItem
 - mmc/IResultOwnerData::FindItem
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
 - IResultOwnerData.FindItem
---

# IResultOwnerData::FindItem


## -description

The <b>IResultOwnerData::FindItem</b> method finds the next item in a virtual list matching a specified string.

## -parameters

### -param pFindInfo [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/ns-mmc-resultfindinfo">RESULTFINDINFO</a> structure.

### -param pnFoundIndex [out]

A pointer to the returned index of the item found. The value is –1 if no items are found.

## -returns

This method can return one of these values.

## -remarks

Because the snap-in maintains all the item data for a virtual list, the snap-in must implement 
FindItem to allow navigation by partial name typing. The console calls 
FindItem to find the next match each time the user types a printable character. The console handles the character accumulation and timing functions, passing the snap-in the current partial name in each 
FindItem call.

## -see-also

<a href="/windows/desktop/api/mmc/ns-mmc-resultfindinfo">RESULTFINDINFO</a>