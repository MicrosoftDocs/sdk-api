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

# ITravelLog::InsertMenuEntries


## -description


Deprecated. Inserts entries into the specified menu.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the menu.


### -param nPos [in]

Type: <b>int</b>

The position in the menu to insert the entries.


### -param idFirst [in]

Type: <b>int</b>

The ID of the first entry to be inserted.


### -param idLast [in]

Type: <b>int</b>

The ID of the last entry to be inserted. The difference between <i>idFirst</i> and <i>idLast</i> is the maximum number of entries that can be inserted into the menu.


### -param dwFlags [in]

Type: <b>DWORD</b>

The types of entries to add to the menu. Includes the following:



#### TLMENUF_INCLUDECURRENT

Include the current page.



#### TLMENUF_CHECKCURRENT

Add a check mark next to the entry of the current page.



#### TLMENUF_BACK

Default. The previous pages.



#### TLMENUF_FORE

The next pages.



#### TLMENUF_BACKANDFORTH

Previous, current, and next pages.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



