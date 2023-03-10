---
UID: NF:mmc.IResultData.InsertItem
title: IResultData::InsertItem (mmc.h)
description: The IResultData::InsertItem method enables the snap-in to add a single new item to the result pane view.
helpviewer_keywords: ["IResultData interface [MMC]","InsertItem method","IResultData.InsertItem","IResultData2 interface [MMC]","InsertItem method","IResultData2::InsertItem","IResultData::InsertItem","InsertItem","InsertItem method [MMC]","InsertItem method [MMC]","IResultData interface","InsertItem method [MMC]","IResultData2 interface","_slate_iresultdata_insertitem","mmc.iresultdata_insertitem","mmc/IResultData2::InsertItem","mmc/IResultData::InsertItem"]
old-location: mmc\iresultdata_insertitem.htm
tech.root: mmc
ms.assetid: c354e718-ea9a-4d50-8a77-776500b86d25
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],InsertItem method, IResultData.InsertItem, IResultData2 interface [MMC],InsertItem method, IResultData2::InsertItem, IResultData::InsertItem, InsertItem, InsertItem method [MMC], InsertItem method [MMC],IResultData interface, InsertItem method [MMC],IResultData2 interface, _slate_iresultdata_insertitem, mmc.iresultdata_insertitem, mmc/IResultData2::InsertItem, mmc/IResultData::InsertItem
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
 - IResultData::InsertItem
 - mmc/IResultData::InsertItem
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
 - IResultData.InsertItem
 - IResultData2.InsertItem
---

# IResultData::InsertItem


## -description

The <b>IResultData::InsertItem</b> method enables the snap-in to add a single new item to the result pane view.

## -parameters

### -param item [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure that contains information about the item to be added.

After the item is inserted, a unique identifier (an item ID) is assigned to it by MMC and returned through the <b>itemID</b> member of the structure pointed to by the item parameter. Be aware that the <b>itemID</b> value is the <b>HRESULTITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as <a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-getitem">IResultData::GetItem</a>.

If this identifier is not stored, it can be looked up using 
<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-finditembylparam">IResultData::FindItemByLParam</a>.

## -returns

This method can return one of these values.

## -remarks

The mask and all appropriate associated fields in the 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure should be filled out. Subitems cannot be inserted but can be set. The <b>nCol</b> member of the item structure must therefore be zero.

The str member of 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> must be set to <b>MMC_CALLBACK</b>.

After the item is inserted, a unique identifier (an item ID) is assigned to it by MMC and returned through the <b>itemID</b> member of the structure pointed to by the item parameter. Be aware that the <b>itemID</b> value is the <b>HRESULTITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as <a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-getitem">IResultData::GetItem</a>.

If this identifier is not stored, it can be identified using 
<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-finditembylparam">IResultData::FindItemByLParam</a>.

This method does not support virtual lists.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>