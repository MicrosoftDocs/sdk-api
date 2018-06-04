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

# IUIAutomationPatternHandler::CreateClientWrapper


## -description


Creates an object that enables a client application to interact with a custom <i>control pattern</i>.


## -parameters




### -param pPatternInstance [in]

Type: <b><a href="https://msdn.microsoft.com/54791426-3905-49d6-aaaf-87a18d3ef659">IUIAutomationPatternInstance</a>*</b>

A pointer to the instance of the control pattern that will be used by the wrapper. 


### -param pClientWrapper [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives a pointer to the wrapper object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The wrapper object exposes methods and properties of the <i>control pattern</i>. The implementation of the wrapper class passes these calls to Microsoft UI Automation by calling <a href="https://msdn.microsoft.com/a3c1aa20-c512-4752-8da6-c8e86bd56beb">CallMethod</a> and <a href="https://msdn.microsoft.com/cb64569f-799b-4e9a-a9f4-84513b98c941">GetProperty</a>. 
			




## -see-also




<a href="https://msdn.microsoft.com/6d0edd8e-3fd4-47d6-ab53-582eb81f38bd">IUIAutomationPatternHandler</a>
 

 

