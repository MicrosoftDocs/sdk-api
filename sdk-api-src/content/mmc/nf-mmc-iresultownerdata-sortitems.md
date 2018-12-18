---
UID: NF:mmc.IResultOwnerData.SortItems
title: IResultOwnerData::SortItems
author: windows-sdk-content
description: Sorts the items of a virtual result list.
old-location: mmc\iresultownerdata_sortitems.htm
tech.root: mmc
ms.assetid: 5326e935-cb6c-4f76-8c9b-87d910dbbb0d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IResultOwnerData interface [MMC],SortItems method, IResultOwnerData.SortItems, IResultOwnerData::SortItems, RSI_DESCENDING = 0x0001, RSI_NOSORTICON = 0x0002, SortItems, SortItems method [MMC], SortItems method [MMC],IResultOwnerData interface, _slate_iresultownerdata_sortitems, mmc.iresultownerdata_sortitems, mmc/IResultOwnerData::SortItems
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultOwnerData.SortItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultOwnerData::SortItems


## -description


The <b>IResultOwnerData::SortItems</b> method sorts the items of a virtual result list.


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

A user parameter passed in an 
<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a> call, <b>NULL</b> if the user initiated the sort.


## -returns



This method can return one of these values.




## -remarks



Because the snap-in maintains all the item data storage for a virtual list, the list does not support sorting. The console calls this function when the user clicks the header item of a virtual list or when the snap-in calls 
<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a>.

MMC calls <b>IResultOwnerData::SortItems</b> with the same sort options that were passed by the snap-in in the call to <a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a>.




## -see-also




<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a>
 

 

