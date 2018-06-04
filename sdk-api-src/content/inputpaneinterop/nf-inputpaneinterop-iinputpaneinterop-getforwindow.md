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

# IInputPaneInterop::GetForWindow


## -description


Gets an instance of an <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object for the specified window.


## -parameters




### -param appWindow [in]

The window for which you want to get the <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object.


### -param riid [in]

The interface identifier for the interface that you want to get in the <i>inputPane</i> parameter. This value is typically <b>IID_IInputPane</b> or <b>IID_IInputPane2</b>, as defined in Windows.UI.ViewManagement.h.


### -param inputPane [out, retval]

The <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object for the window that the <i>appWindow</i> parameter specifies. This parameter is typically a pointer to an <b>IInputPane</b> or <b>IInputPane2</b> interface, as defined in Windows.UI.ViewManagement.idl.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/DAE4705C-B786-44D4-8B03-1523EFC4C190">IInputPaneInterop</a>



<a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a>
 

 

