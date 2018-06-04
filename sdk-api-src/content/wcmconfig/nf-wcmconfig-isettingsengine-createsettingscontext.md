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

# ISettingsEngine::CreateSettingsContext


## -description


Creates a settings context.


## -parameters




### -param Flags [in]

The value of the Flags parameter may be 0, indicating "normal mode"  or 0x00000001, indicating <b>LIMITED_VALIDATION_MODE</b>. In normal mode, the settings context validates any changes made to list items against the current state of the target image. For example, if an  attempt is made to create a list element that already exists in the image, the create operation fails. In <b>LIMITED_VALIDATION_MODE</b>, contradictory data is not accepted. You cannot modify and then add a list item. However, no attempt is made to verify the changes made against the current state of the system. Only use <b>LIMITED_VALIDATION_MODE</b> when the intention is to author a context which is to be serialized. Do not specify this flag when creating a context to be used for <a href="https://msdn.microsoft.com/459a97fb-e5fb-42a5-998d-84631fec2e6f">ISettingsEngine::ApplySettingsContext</a>. If used, the context may not be sufficiently validated and may fail during an application.


### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param SettingsContext [out]

A pointer to an <a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a> object that represents the created context.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. This method may return <b>E_OUTOFMEMORY</b> if there were insufficient resources to create the <a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a> object.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

