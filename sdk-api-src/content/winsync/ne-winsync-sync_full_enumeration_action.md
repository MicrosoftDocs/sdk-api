---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0004
title: SYNC_FULL_ENUMERATION_ACTION
author: windows-sdk-content
description: Represents the action to be taken by an application in response to ISyncCallback::OnFullEnumerationNeeded.
old-location: winsync\sync_full_enumeration_action.htm
tech.root: winsync
ms.assetid: 4fdb7123-d8c8-4ed7-9009-0e772252bbb7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SFEA_ABORT, SFEA_FULL_ENUMERATION, SFEA_PARTIAL_SYNC, SYNC_FULL_ENUMERATION_ACTION, SYNC_FULL_ENUMERATION_ACTION enumeration [Windows Sync], winsync.sync_full_enumeration_action, winsync/SFEA_ABORT, winsync/SFEA_FULL_ENUMERATION, winsync/SFEA_PARTIAL_SYNC, winsync/SYNC_FULL_ENUMERATION_ACTION
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - SYNC_FULL_ENUMERATION_ACTION
product: Windows
targetos: Windows
req.typenames: SYNC_FULL_ENUMERATION_ACTION
req.redist: 
---

# SYNC_FULL_ENUMERATION_ACTION enumeration


## -description


Represents the action to be taken by an application in response to <a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback::OnFullEnumerationNeeded</a>.


## -enum-fields




### -field SFEA_FULL_ENUMERATION

Perform a full enumeration. This is the default option when the application does not register an <a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback</a> interface.


### -field SFEA_PARTIAL_SYNC

Perform a partial synchronization. When this option is specified, the learned knowledge is applied as single item exceptions.


### -field SFEA_ABORT

Cancel the synchronization session. All methods will return errors as if they were canceled.


## -see-also




<a href="https://msdn.microsoft.com/f52ddaf2-9ce2-4ebb-bace-024c059b2594">ISyncCallback::OnFullEnumerationNeeded</a>



<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

