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

# IVisualProperties::SetTheme


## -description


Sets the specified theme.


## -parameters




### -param pszSubAppName [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that contains the application name to use in place of the calling application's name. If this parameter is <b>NULL</b>, the calling application's name is used.


### -param pszSubIdList [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that contains a semicolon-separated list of CLSID names for use in place of the actual list passed by the window's class. If this parameter is <b>NULL</b>, the ID list from the calling class is used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



