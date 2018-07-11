---
UID: NS:winsync._SYNC_SESSION_STATISTICS
title: "_SYNC_SESSION_STATISTICS"
author: windows-sdk-content
description: Represents statistics about a single, unidirectional synchronization session.
old-location: winsync\sync_session_statistics.htm
old-project: winsync
ms.assetid: e6d1fe9e-6cf2-414a-9be6-b444af2c7525
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: SYNC_SESSION_STATISTICS, SYNC_SESSION_STATISTICS structure [Windows Sync], _SYNC_SESSION_STATISTICS, winsync.sync_session_statistics, winsync/SYNC_SESSION_STATISTICS
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNC_SESSION_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - SYNC_SESSION_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SYNC_SESSION_STATISTICS structure


## -description


Represents statistics about a single, unidirectional synchronization session.


## -struct-fields




### -field dwChangesApplied

The total number of changes that were successfully applied during the synchronization session. This value is the sum of item changes plus change unit changes.




### -field dwChangesFailed

The total number of changes that were not applied during a session. This value is the sum of item changes plus change unit changes.


## -see-also




<a href="https://msdn.microsoft.com/528a109a-9c11-4e20-b3d5-9bb7241d02b6">IKnowledgeSyncProvider::ProcessChangeBatch Method</a>



<a href="https://msdn.microsoft.com/7d34bc48-377c-4249-a26e-0802dee0b53c">IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch Method</a>



<a href="https://msdn.microsoft.com/eed33384-f8bd-4a3a-8d04-b59c534f9114">Windows Sync Structures</a>
 

 

