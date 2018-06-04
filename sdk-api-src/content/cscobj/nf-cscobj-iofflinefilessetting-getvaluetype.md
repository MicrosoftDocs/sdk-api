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

# IOfflineFilesSetting::GetValueType


## -description


Retrieves the data type of a particular Offline Files setting.


## -parameters




### -param pType [out]

Receives a value from the <a href="https://msdn.microsoft.com/37569197-efd3-4e4e-953a-3bbd2cb07d5a">OFFLINEFILES_SETTING_VALUE_TYPE</a> enumeration that describes the data type of the setting value.


## -returns



S_OK if the scope is returned successfully or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

