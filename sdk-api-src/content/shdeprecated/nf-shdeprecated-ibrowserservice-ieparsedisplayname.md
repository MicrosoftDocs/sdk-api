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

# IBrowserService::IEParseDisplayName


## -description


Deprecated. Parses a URL into a pointer to an item identifier list (PIDL).


## -parameters




### -param uiCP [in]

Type: <b>UINT</b>

A value of type <b>UINT</b> that indicates the code page (for example, CP_ACP, the system default code page) to use in the parsing.


### -param pwszPath [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the URL as a Unicode string.


### -param ppidlOut [out]

Type: <b>LPITEMIDLIST*</b>

The PIDL created from the parsed URL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



