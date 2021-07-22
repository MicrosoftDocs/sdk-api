---
UID: NN:mmc.IResultData
title: IResultData (mmc.h)
description: The IResultData interface enables a user to add, remove, find, and modify items associated with the result view pane. It also enables the manipulation of the view style of the result view pane.
helpviewer_keywords: ["IResultData","IResultData interface [MMC]","IResultData interface [MMC]","described","_slate_iresultdata","mmc.iresultdata","mmc/IResultData"]
old-location: mmc\iresultdata.htm
tech.root: mmc
ms.assetid: 58f8bcdb-b062-4048-92fc-eb652ce62c5b
ms.date: 12/05/2018
ms.keywords: IResultData, IResultData interface [MMC], IResultData interface [MMC],described, _slate_iresultdata, mmc.iresultdata, mmc/IResultData
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
 - IResultData
 - mmc/IResultData
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
 - IResultData
---

# IResultData interface


## -description

The 
<b>IResultData</b> interface enables a user to add, remove, find, and modify items associated with the result view pane. It also enables the manipulation of the view style of the result view pane.

The 
<b>IResultData</b> interface was designed to give the impression that the result view pane would be used by only one component, but components should be aware that the result view pane can, in fact, be shared by several components. All item manipulations are performed through the use of an item ID assigned when the item is inserted. This ID is guaranteed to be both static and unique for the life of the item. When an item is deleted, the ID is freed and can be used by other new items in the list. You should never keep an item ID around after its associated item has been deleted.

The 
<b>IResultData</b> interface handles virtual (owner data) lists as well. Because of the nature of virtual lists, not all methods apply and some methods have limited functionality. These differences are detailed in the descriptions of individual methods. The primary difference in handling virtual lists it that because the console does not maintain any storage for virtual items, it does not provide item IDs. Instead virtual list items are identified by their list position (index).

## -inheritance

The <b>IResultData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultData</b> also has these types of members:

