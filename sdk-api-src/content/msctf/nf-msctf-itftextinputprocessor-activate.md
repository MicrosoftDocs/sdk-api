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

# ITfTextInputProcessor::Activate


## -description




## -parameters




### -param ptim [in]

Pointer to the <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> interface for the thread manager that owns the text service.


### -param tid [in]

Specifies the client identifier for the text service.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TSF calls this method after creating an instance of a text service with a call to <a href="_com_cocreateinstance">CoCreateInstance</a>. This enables operations necessary to start the text service.

This method usually adds a reference to the thread manager for the session and advise sinks for events that involve the text service, such as change of focus, keystrokes, and window events. It also customizes the language bar for the text service.

The corresponding <a href="https://msdn.microsoft.com/427190fc-f246-47c6-84e0-a28808a86b6b">ITfTextInputProcessor::Deactivate</a> method that shuts down the text service must release all references to the <i>ptim</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/d3fd296b-0009-4fc2-bf91-0ad31454f0e8">ITfTextInputProcessor
      </a>



<a href="https://msdn.microsoft.com/427190fc-f246-47c6-84e0-a28808a86b6b">
        ITfTextInputProcessor::Deactivate
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">
        ITfThreadMgr
      </a>
 

 

