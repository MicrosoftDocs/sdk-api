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

# IEnumExplorerCommand::Next


## -description


Retrieves a specified number of elements that directly follow the current element.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of elements to fetch.


### -param pUICommand [out]

Type: <b><a href="https://msdn.microsoft.com/61e94e50-9e12-4a2c-a6c7-64a9181f80b8">IExplorerCommand</a>**</b>

Address of an <a href="https://msdn.microsoft.com/61e94e50-9e12-4a2c-a6c7-64a9181f80b8">IExplorerCommand</a> interface pointer array of <i>celt</i> elements that, when this method returns, is an array of pointers to the retrieved elements.


### -param pceltFetched [out, optional]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of elements actually retrieved. This pointer can be <b>NULL</b> if this information is not needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



