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

# _SEARCH_NOTIFICATION_PRIORITY enumeration


## -description


Indicates the priority of processing an item that has changed.


## -enum-fields




### -field SEARCH_NORMAL_PRIORITY

The changed item is added to the end of the indexer's queue.


### -field SEARCH_HIGH_PRIORITY

The changed item is placed ahead of other queued items in the indexer's queue, to be processed as soon as possible.


## -remarks



Set the <b>priority</b> member of the <a href="https://msdn.microsoft.com/83ed1c76-7210-4d0b-a6e2-461bc331e168">SEARCH_ITEM_CHANGE</a> structure to one of these flags.

As the indexer crawls, it builds a list of items that need to be indexed. These flags indicate the placement of changed items in the indexer's queue. Higher priority items are placed at the front of the queue.



