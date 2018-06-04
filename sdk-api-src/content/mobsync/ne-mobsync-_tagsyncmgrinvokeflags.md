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

# _tagSYNCMGRINVOKEFLAGS enumeration


## -description


The 
<b>SYNCMGRINVOKEFLAGS</b> enumeration value specifies how the Sync Manager is to be invoked in the 
<a href="https://msdn.microsoft.com/7a646d11-a84c-44c1-b52b-ffd364cc2ac3">ISyncMgrSynchronizeInvoke::UpdateItems</a> method.


## -enum-fields




### -field SYNCMGRINVOKE_STARTSYNC

Immediately start the synchronization without displaying the <b>Choice</b> dialog box.


### -field SYNCMGRINVOKE_MINIMIZED

Indicates that the <b>Choice</b> dialog should be minimized by default.


## -see-also




<a href="https://msdn.microsoft.com/7a646d11-a84c-44c1-b52b-ffd364cc2ac3">ISyncMgrSynchronizeInvoke::UpdateItems</a>
 

 

