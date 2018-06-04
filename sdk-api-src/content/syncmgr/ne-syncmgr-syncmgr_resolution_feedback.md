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

# SYNCMGR_RESOLUTION_FEEDBACK enumeration


## -description


Describes Sync Manager resolution feedback. Used by <a href="https://msdn.microsoft.com/5b77217d-5c63-41be-b4df-338714a90fb9">ISyncMgrResolutionHandler</a>.


## -enum-fields




### -field SYNCMGR_RF_CONTINUE

Proceed to the next conflict.


### -field SYNCMGR_RF_REFRESH

<b>Apply to All</b> is stopped and the dialog will be displayed for this conflict.


### -field SYNCMGR_RF_CANCEL

 Cancels resolution of any more conflicts in the set.

