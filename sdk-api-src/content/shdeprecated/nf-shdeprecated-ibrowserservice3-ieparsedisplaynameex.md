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

# IBrowserService3::IEParseDisplayNameEx


## -description


Deprecated. Parses a URL into a pointer to an item identifier list (PIDL).


## -parameters




### -param uiCP

Type: <b>UINT</b>

The code page (for example, CP_ACP, the system default code page).


### -param pwszPath

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the URL to parse, as a Unicode string.


### -param dwFlags

Type: <b>DWORD</b>

The following value, if desired.



#### IEPDN_BINDINGUI (0x00000001)

Display a UI element during binding.


### -param ppidlOut

Type: <b>LPITEMIDLIST*</b>

The PIDL created from the parsed URL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method replaces <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IEParseDisplayName</a>.



