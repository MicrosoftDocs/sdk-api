---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOfflineFilesSyncProgress::SyncItemResult


## -description



    Reports that an item has been processed during the synchronization operation.  This method is called even if the operation was unsuccessful.  Check the value received in the <i>hrResult</i> parameter to determine whether the operation was successful.


## -parameters




### -param pszFile [in]

Receives the fully qualified UNC path of the item that was processed.


### -param hrResult [in]

Receives the result of the operation for the item.  Contains S_OK if the operation completed successfully or an error value otherwise.


### -param pErrorInfo [in]

Receives a pointer to an instance of the <a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a> interface that provides detailed information about the result of the sync operation.


### -param pResponse [out]

Set this parameter to a value from the <a href="https://msdn.microsoft.com/a4b16256-7f6a-4e26-8cf2-3ef7c59ac3af">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a>
 

 

