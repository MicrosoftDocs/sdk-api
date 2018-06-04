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

# IFileOperation::PerformOperations


## -description


Executes all selected operations.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Note that if the operation was canceled by the user, this method can still return a success code. Use the <a href="https://msdn.microsoft.com/988f78a8-3a50-44d8-9214-7cf71be72d38">GetAnyOperationsAborted</a> method to determine if this was the case.




## -remarks



This method is called last to execute those actions that have been specified earlier by calling their individual methods. For instance, <a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">RenameItem</a> does not rename the item, it simply sets the parameters. The actual renaming is done when you call <b>PerformOperations</b>.




## -see-also




<a href="https://msdn.microsoft.com/5d2d05c3-525d-4113-bb08-63395facf191">FinishOperations</a>



<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/8b9e4423-ead7-44be-b960-5ee83025f42a">StartOperations</a>
 

 

