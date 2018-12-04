---
UID: NF:mmc.IResultData.Sort
title: IResultData::Sort
author: windows-sdk-content
description: Sorts all items in the result pane.
old-location: mmc\iresultdata_sort.htm
tech.root: mmc
ms.assetid: 457eccaf-3727-4b29-a38b-9f009749673e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IResultData interface [MMC],Sort method, IResultData.Sort, IResultData2 interface [MMC],Sort method, IResultData2::Sort, IResultData::Sort, RSI_DESCENDING = 0x0001, RSI_NOSORTICON = 0x0002, Sort, Sort method [MMC], Sort method [MMC],IResultData interface, Sort method [MMC],IResultData2 interface, _slate_iresultdata_sort, mmc.iresultdata_sort, mmc/IResultData2::Sort, mmc/IResultData::Sort
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
 - IResultData.Sort
 - IResultData2.Sort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultData::Sort


## -description


The <b>IResultData::Sort</b> method sorts all items in the result pane.


## -parameters




### -param nColumn [in]

An index of the column header clicked.


### -param dwSortOptions [in]

The sort options to be used during the sort operation. This value can be a combination of the following:



#### RSI_DESCENDING = 0x0001

The sort should be in descending order. The default is to sort in ascending order.



#### RSI_NOSORTICON = 0x0002

Instructs MMC to remove the sort arrow icon. This option is useful when the snap-in performs a custom sort operation.


### -param lUserParam [in]

A value that specifies information determined by the user. This parameter can contain a variety of entries such as including sort order or context information.


## -returns



This method can return one of these values.




## -remarks



If your snap-in implements the 
<a href="https://msdn.microsoft.com/7a68713c-2de5-4944-a617-0b2d46c23eea">IResultDataCompare</a> or the 
<a href="https://msdn.microsoft.com/e4b305e4-4649-42f4-86f4-3c12e5aa5337">IResultDataCompareEx</a> interface, MMC calls the interface's 
Compare method to allow the snap-in to compare list items. Otherwise, MMC uses a default string-compare function.

There is no sorting function for a virtual list. To allow virtual list sorting the snap-in must implement the 
<a href="https://msdn.microsoft.com/184f3783-9000-45aa-867b-580800b560b3">IResultOwnerData</a> interface. When <b>IResultData::Sort</b> is called, MMC forwards the call to 
<a href="https://msdn.microsoft.com/5326e935-cb6c-4f76-8c9b-87d910dbbb0d">IResultOwnerData::SortItems</a>.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>



<a href="https://msdn.microsoft.com/00d18ba5-589f-4a70-b331-ba9c7d5164c5">IResultDataCompare::Compare</a>



<a href="https://msdn.microsoft.com/5326e935-cb6c-4f76-8c9b-87d910dbbb0d">IResultOwnerData::SortItems</a>
 

 

