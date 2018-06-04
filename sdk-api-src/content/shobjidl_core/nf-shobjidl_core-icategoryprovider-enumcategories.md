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

# ICategoryProvider::EnumCategories


## -description


Gets the enumerator for the list of GUIDs that represent categories.


## -parameters




### -param penum [out]

Type: <b>IEnumGUID**</b>

When this method returns, contains the address of a pointer to an <b>IEnumGUID</b> interface that specifies a list of GUIDs that represent categories.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the case of the system folder view object, <b>ICategoryProvider::EnumCategories</b> is used to obtain additional categories that are not associated with a column. When the list of category GUIDs is returned through <i>penum</i>, the UI attempts to retrieve the name of each category. That name is then displayed as a category choice. In the case of Windows XP, that choice appears in the folder's <b>Arrange Icons By</b> menu.



