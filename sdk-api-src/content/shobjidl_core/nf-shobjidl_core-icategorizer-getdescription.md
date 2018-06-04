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

# ICategorizer::GetDescription


## -description


Gets the name of a categorizer, such as <i>Group By Device Type</i>, that can be displayed in the UI.


## -parameters




### -param pszDesc [out]

Type: <b>LPWSTR</b>

When this method returns, contains a pointer to a string of length <i>cch</i> that contains the categorizer name.


### -param cch [in]

Type: <b>UINT</b>

The number of characters in the <i>pszDesc</i> buffer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the case of the system folder view object, if the description at <i>pszDesc</i> matches one of the category names listed in the folder's <b>Arrange Icons By</b> menu, a dot is placed by that name when the menu is displayed, either through the <b>View</b> menu or through the context menu.



