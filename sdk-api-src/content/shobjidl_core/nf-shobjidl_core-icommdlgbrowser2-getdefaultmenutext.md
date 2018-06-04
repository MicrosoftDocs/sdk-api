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

# ICommDlgBrowser2::GetDefaultMenuText


## -description


Called by the Shell view to get the default shortcut menu text.


## -parameters




### -param ppshv




### -param pszText

Type: <b>WCHAR*</b>

A pointer to a buffer that is used by the Shell browser to return the default shortcut menu text.


### -param cchMax

Type: <b>int</b>

The size of the <i>pszText</i> buffer, in characters. It should be at least the maximum allowable path length (MAX_PATH) in size.


#### - pshv

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface of the hosted view.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if a new default shortcut menu text was returned in <i>pshv</i>. If S_FALSE is returned, use the normal default text. Otherwise, returns a standard COM error value.



