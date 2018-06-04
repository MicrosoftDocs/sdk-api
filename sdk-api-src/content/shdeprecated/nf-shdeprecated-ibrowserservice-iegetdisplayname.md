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

# IBrowserService::IEGetDisplayName


## -description


Deprecated. Retrieves the URL that corresponds to a pointer to an item identifier list (PIDL).


## -parameters




### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

The PIDL for which to get the corresponding URL.


### -param pwszName [out]

Type: <b>LPWSTR</b>

A pointer to a buffer of at least INTERNET_MAX_URL_LENGTH characters to receive the URL.


### -param uFlags [in]

Type: <b>UINT</b>

One of the following values specifying the form of the retrieved URL.



#### SHGDN_NORMAL (0)

The URL is relative to the folder from which the request was made. SHGDN_NORMAL is equivalent to <b>NULL</b> and therefore should not be combined with other flags.



#### SHGDN_FORADDRESSBAR (0)

The URL is suitable for display in an address bar combo box.



#### SHGDN_FORPARSING (0)

The URL can be used for parsing.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



