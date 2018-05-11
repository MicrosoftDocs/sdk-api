---
UID: NS:winsync._SYNC_RANGE
title: "_SYNC_RANGE"
author: windows-driver-content
description: Represents a range of item IDs.
old-location: winsync\sync_range.htm
old-project: winsync
ms.assetid: d3e4a4f4-4a67-4dce-a81a-3861dcf788e6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SYNC_RANGE, SYNC_RANGE structure [Windows Sync], _SYNC_RANGE, winsync.sync_range, winsync/SYNC_RANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNC_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winsync.h
api_name:
-	SYNC_RANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SYNC_RANGE structure


## -description


Represents a range of item IDs.


## -struct-fields




### -field pbClosedLowerBound

The closed lower bound of item IDs that are contained in the range.


### -field pbClosedUpperBound

The closed upper bound of item IDs that are contained in the range.


## -see-also




<a href="https://msdn.microsoft.com/7d34bc48-377c-4249-a26e-0802dee0b53c">IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch Method</a>



<a href="https://msdn.microsoft.com/3c09284f-9866-49a4-adeb-561af3351ada">ISyncKnowledge::ProjectOntoRange Method</a>



<a href="https://msdn.microsoft.com/eed33384-f8bd-4a3a-8d04-b59c534f9114">Windows Sync Structures</a>
 

 

