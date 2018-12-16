---
UID: NF:mmc.IColumnData.SetColumnConfigData
title: IColumnData::SetColumnConfigData
author: windows-sdk-content
description: The IColumnData::SetColumnConfigData method enables a snap-in to set the persisted width, order, and hidden status of columns in a column set.
old-location: mmc\icolumndata_setcolumnconfigdata.htm
tech.root: mmc
ms.assetid: 2f6727bd-b7ba-4e91-9dce-53605b0b6fe1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IColumnData interface [MMC],SetColumnConfigData method, IColumnData.SetColumnConfigData, IColumnData::SetColumnConfigData, SetColumnConfigData, SetColumnConfigData method [MMC], SetColumnConfigData method [MMC],IColumnData interface, _slate_icolumndata_setcolumnconfigdata, mmc.icolumndata_setcolumnconfigdata, mmc/IColumnData::SetColumnConfigData
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
 - IColumnData.SetColumnConfigData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IColumnData::SetColumnConfigData


## -description


The <b>IColumnData::SetColumnConfigData</b> method enables a snap-in to set the persisted width, order, and hidden status of columns in a column set.


## -parameters




### -param pColID [in]

A pointer to an 
<a href="https://msdn.microsoft.com/eb08f699-74bc-445d-96b7-678abbd366b3">SColumnSetID</a> structure that contains the ID of the column set whose data is to be set.


### -param pColSetData [in]

A pointer to an 
<a href="https://msdn.microsoft.com/15088a2f-3dfc-4af4-bcae-e7e9e456df8b">MMC_COLUMN_SET_DATA</a> structure that contains the number of columns in the column set as well as the column data to be set.


## -returns



This method can return one of these values.




## -remarks



If the user selects a scope item, and the snap-in then calls <b>IColumnData::SetColumnConfigData</b> to modify the column configuration data of the list view of the selected item. MMC will apply the changes to the list view only after the user has deselected and then reselected the item. Be aware that MMC also applies the changes to all column sets with the same ID, so if the user selects a different item with the same column set ID, MMC will also apply the persisted data to it.

Calling 
<b>IColumnData::SetColumnConfigData</b> clears the previously stored sort information and column configuration information.




## -see-also




<a href="https://msdn.microsoft.com/fb2b8863-c476-4997-915d-329cf66fd945">IColumnData</a>



<a href="https://msdn.microsoft.com/4da79fd1-f887-447c-89fd-d5044bd5751c">Using IColumnData</a>
 

 

