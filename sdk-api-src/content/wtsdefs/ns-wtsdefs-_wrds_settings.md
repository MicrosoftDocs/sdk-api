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

# _WRDS_SETTINGS structure


## -description


Contains policy-related setting information for a remote session.

This structure is used in the <a href="https://msdn.microsoft.com/3680a001-e162-4930-985f-5c50c2e8a8b9">IWRdsProtocolSettings</a> interface and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method of the <a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a> interface.


## -struct-fields




### -field WRdsSettingType

The category of settings contained (machine group policy, user group policy, or user security accounts manager).


### -field WRdsSettingLevel

The setting level.


### -field WRdsSetting

A structure that contains the policy setting states and values.

A structure that contains the policy setting states and values.


### -field WRdsSetting.switch_is

 


### -field WRdsSetting.switch_is.WRdsSettingLevel

 



