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

# IUIAutomationChangesEventHandler::HandleChangesEvent


## -description


Handles a Microsoft UI Automation changes event.


## -parameters




### -param sender [in]

A pointer to the element that raised the event.


### -param uiaChanges [in]

A collection of pointers to <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures.


### -param changesCount [in]

The number of changes that occurred. This is the number of <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures pointed to by the <i>uiaChanges</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by calling <a href="https://msdn.microsoft.com/E479ACCA-9372-463F-A992-8030E33A2341">AddChangesEventHandler</a>.




## -see-also




<a href="https://msdn.microsoft.com/8DCF8826-B688-416C-9195-34E0290054AA">IUIAutomationChangesEventHandler</a>
 

 

