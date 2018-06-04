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

# IOpenControlPanel::Open


## -description


Opens the specified Control Panel item, optionally to a specific page.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the item's canonical name as a Unicode string. This parameter is optional and can be <b>NULL</b>. If the calling application passes <b>NULL</b>, then the Control Panel itself opens. For a complete list of Control Panel item canonical names, see <a href="https://msdn.microsoft.com/A02DFC9F-646D-40d8-901C-7239A820DE2C">Canonical Names of Control Panel Items</a>.


### -param pszPage [in]

Type: <b>LPCWSTR</b>

A pointer to the name of the page within the item to display. This string is appended to the end of the path for Shell folder Control Panel items or appended as a command-line parameter for Control Panel (.cpl) file items. This parameter can be <b>NULL</b>, in which case the first page is shown.


### -param punkSite [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the site for navigating in-frame for Shell folder Control Panel items. This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="ffd6c6de-2c65-4ab1-b1fa-27abe6a10342">Developing for the Control Panel</a>



<a href="https://msdn.microsoft.com/fbf86553-7aa1-4a0f-9775-5f71f41b1705">IOpenControlPanel</a>
 

 

