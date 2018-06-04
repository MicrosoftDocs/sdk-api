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

# _CLUSTER_READ_BATCH_COMMAND structure


## -description


Represents a result for a single command in a read batch.


## -struct-fields




### -field Command

The command result status, which can be one of these values.



#### CLUSREG_READ_VALUE (8)

The result structure has content for the requested value. The <b>dwOptions</b> member is set to the registry value type.



#### CLUSREG_READ_ERROR (9)

The value was missing, or another error occurred during read. The <b>dwOptions</b> member contains the actual error type.


### -field dwOptions

The registry value type or the read error type, depending on the <i>Command</i> result.


### -field wzSubkeyName

The name of the key requested in the read command.


### -field wzValueName

The name of the value requested in the read command.


### -field lpData

A pointer to value data.


### -field cbData

The count, in bytes, of the <i>lpData</i> value data.


## -remarks



The pointers in the <b>CLUSTER_READ_BATCH_COMMAND</b> structure are valid until the read batch result handle is closed by the <a href="https://msdn.microsoft.com/C8CC4292-A7CC-4613-B5A8-B504E804E00E">ClusterRegCloseReadBatchReply</a> function.

Errors from read commands are independent from each other.




## -see-also




<a href="https://msdn.microsoft.com/C8CC4292-A7CC-4613-B5A8-B504E804E00E">ClusterRegCloseReadBatchReply</a>



<a href="https://msdn.microsoft.com/4E0DEB5C-36AA-480C-913C-235DE9AEA58D">ClusterRegReadBatchReplyNextCommand</a>
 

 

