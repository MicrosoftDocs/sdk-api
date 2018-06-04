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

# IAssocHandler::GetIconLocation


## -description


Retrieves the location of the icon associated with the application.


## -parameters




### -param ppszPath [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated, Unicode string that contains the path to the application's icon.


### -param pIndex [out]

Type: <b>int*</b>

When this method returns, contains a pointer to the index of the icon within the resource named in <i>ppszPath</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the icon cannot be found, the function will return the path to the executable, and an icon index of zero.

For performance reasons, an application may use the Shell image cache to retrieve the icon, rather than loading the icon directly from the path returned.  The path and icon index can be passed directly to <a href="https://msdn.microsoft.com/f0d4dd1f-a41c-4dd0-9713-e3aec48ff101">Shell_GetCachedImageIndex</a>. One benefit of this is that the Shell cache can provide a default icon in the event that no icon was available for the application.



