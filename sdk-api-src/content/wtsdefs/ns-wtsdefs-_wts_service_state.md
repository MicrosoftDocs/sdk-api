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

# _WTS_SERVICE_STATE structure


## -description


Contains information about changes in the state of the Remote Desktop Services service.


## -struct-fields




### -field RcmServiceState

A value of the <a href="https://msdn.microsoft.com/5f022d92-b048-4c87-918c-6e8f297cc1a6">WTS_RCM_SERVICE_STATE</a> enumeration type that specifies whether the service is starting or stopping.


### -field RcmDrainState

A value of the <a href="https://msdn.microsoft.com/bb033bef-e325-42d0-8879-9a2151e43e91">WTS_RCM_DRAIN_STATE</a> enumeration type that specifies whether the  RD Session Host server is changing its drain state.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/303a53b3-b297-486c-9422-706ec60441f2">NotifyServiceStateChange</a> method.



