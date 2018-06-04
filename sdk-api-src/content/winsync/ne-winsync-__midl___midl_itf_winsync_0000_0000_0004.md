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

# __MIDL___MIDL_itf_winsync_0000_0000_0004 enumeration


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
 

 

