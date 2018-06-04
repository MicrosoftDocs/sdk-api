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

# ISettingsItem::GetPath


## -description


Gets the path for the item.


## -parameters




### -param Path [out]

The path to the current setting. This path should be handled as opaque, and should be used only for invocations of <a href="https://msdn.microsoft.com/8b51329e-dc81-46dc-b174-0191e2eea44a">CreateSettingByPath</a>, <a href="https://msdn.microsoft.com/a4270c46-b214-4232-b414-d6b6e4e35635">GetSettingByPath</a>, or <a href="https://msdn.microsoft.com/5613df85-009f-4aab-91bc-797a6cf73cd0">RemoveSettingByPath</a>.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources.




## -see-also




<a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a>
 

 

