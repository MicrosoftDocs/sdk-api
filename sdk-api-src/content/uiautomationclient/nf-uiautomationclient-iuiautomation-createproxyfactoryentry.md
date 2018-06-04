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

# IUIAutomation::CreateProxyFactoryEntry


## -description


Creates a new instance of a proxy factory object.


## -parameters




### -param factory [in]

Type: <b><a href="https://msdn.microsoft.com/cdb2c94e-a5a7-41c3-b847-b23ea077abd3">IUIAutomationProxyFactory</a>*</b>

A pointer to  the proxy factory object.


### -param factoryEntry [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0507deef-35dc-45bb-a7c1-82b84344ee17">IUIAutomationProxyFactoryEntry</a>**</b>

Receives a pointer to the newly created instance of the proxy factory object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <a href="https://msdn.microsoft.com/7a938c1c-a11c-4fdd-a73a-e7656032f21e">IUIAutomationProxyFactoryMapping</a> interface to enter the proxy factory into the table of available proxies. 




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>
 

 

