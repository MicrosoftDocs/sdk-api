---
UID: NF:mmc.IResultData.DeleteItem
title: IResultData::DeleteItem
author: windows-sdk-content
description: Enables the snap-in to delete a single item in the result view pane.
old-location: mmc\iresultdata_deleteitem.htm
tech.root: mmc
ms.assetid: e0e6192a-2cc0-4a90-9793-e425879fcff2
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: DeleteItem, DeleteItem method [MMC], DeleteItem method [MMC],IResultData interface, DeleteItem method [MMC],IResultData2 interface, IResultData interface [MMC],DeleteItem method, IResultData.DeleteItem, IResultData2 interface [MMC],DeleteItem method, IResultData2::DeleteItem, IResultData::DeleteItem, _slate_iresultdata_deleteitem, mmc.iresultdata_deleteitem, mmc/IResultData2::DeleteItem, mmc/IResultData::DeleteItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IResultData.DeleteItem
 - IResultData2.DeleteItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultData::DeleteItem


## -description


The <b>IResultData::DeleteItem</b> method enables the snap-in to delete a single item in the result view pane.


## -parameters




### -param itemID [in]

A value that specifies the unique ID of the item to be deleted. When applied to virtual lists, pass the item index instead of the itemID.


### -param nCol [in]

Not used. Must be zero.


## -returns



This method can return one of these values.




## -remarks



DeleteItem removes an item identified by itemID and nCol. If nCol does not equal zero, the subitem identified by itemID and nCol is cleared of all information. If nCol is equal to zero, the item identified by itemID and all of its subitems are deleted and removed from the list. If a subitem is deleted, itemID remains a valid identifier. However, if the main item is deleted, itemID should be destroyed or released. The same ID can be reassigned by the console to any newly inserted items.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>
 

 

