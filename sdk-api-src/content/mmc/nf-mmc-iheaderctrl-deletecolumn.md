---
UID: NF:mmc.IHeaderCtrl.DeleteColumn
title: IHeaderCtrl::DeleteColumn
author: windows-sdk-content
description: Removes a column from the header of the result view.
old-location: mmc\iheaderctrl_deletecolumn.htm
tech.root: MMC
ms.assetid: 85A4D929-E98B-4C84-9E5C-EA5E41BD0D07
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteColumn, DeleteColumn method [MMC], DeleteColumn method [MMC],IHeaderCtrl interface, IHeaderCtrl interface [MMC],DeleteColumn method, IHeaderCtrl.DeleteColumn, IHeaderCtrl::DeleteColumn, mmc.iheaderctrl_deletecolumn, mmc/IHeaderCtrl::DeleteColumn
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
req.idl: Mmc.idl
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
 - IHeaderCtrl.DeleteColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHeaderCtrl::DeleteColumn


## -description


Removes a column from the header of the result view.


## -parameters




### -param nCol [in]

A zero-based index that identifies the column to be removed.


## -returns



This method can return one of these values.




## -remarks



If a column is removed, all columns with indexes greater than the one removed are adjusted down by one.

MMC does not persist in memory any changes made to a column set due to the action of <b>IHeaderCtrl::DeleteColumn</b>, so snap-ins must update persisted column configuration data after deleting columns from a column set. For more information, see 
<a href="https://msdn.microsoft.com/acec421f-edd4-49b6-a244-7099c524fe75">IHeaderCtrl2 and Column Persistence</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method returns <i>E_FAIL</i> when an item has already been inserted into the result view.




## -see-also




<a href="https://msdn.microsoft.com/64da2c79-2ede-4b17-a706-8e5cc0ade007">IHeaderCtrl</a>



<a href="https://msdn.microsoft.com/acec421f-edd4-49b6-a244-7099c524fe75">IHeaderCtrl2 and Column Persistence</a>
 

 

