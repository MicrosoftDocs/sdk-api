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

# IExplorerBrowser::SetPropertyBag


## -description


Sets the name of the property bag.


## -parameters




### -param pszPropertyBag [in]

Type: <b>LPCWSTR</b>

A pointer to a constant, null-terminated, Unicode string that contains the name of the property bag.
                   View state information that is specific to the application of the client is stored (persisted) using this name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



ExplorerBrowser can retrieve the properties stored in the property bag by calling function <a href="https://msdn.microsoft.com/6852867a-30a5-4d4e-b790-3746104e3ed8">SHGetViewStatePropertyBag</a>. 
 ExplorerBrowser writes to this property bag which is also stored (persisted) in the registry. Persistence occurs automatically when ExplorerBrowser destroys the current view, begins a navigation, or is destroyed. After any of these events, it writes information about the view state in case it has been modified by the user.

 If no properties have been stored, the default view state of the ExplorerBrowser is used. The default view state is the view state that the user has set for a particular location, or if the view state for a location has not been set (never modified by the user), then the default view state is based on the template for the file type (for example, documents, music and pictures) at the location. All Explorer windows use the same sequence to determine the default view state.



