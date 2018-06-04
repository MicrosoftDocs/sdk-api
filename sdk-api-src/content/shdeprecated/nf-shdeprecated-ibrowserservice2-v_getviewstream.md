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

# IBrowserService2::v_GetViewStream


## -description


Deprecated. Returns a stream used to load or save the view state.


## -parameters




### -param pidl

Type: <b>LPCITEMIDLIST</b>

A PIDL that identifies the view.


### -param grfMode

Type: <b>DWORD</b>

Not used.


### -param pwszName

Type: <b>LPCWSTR</b>


          A pointer to a buffer that contains the Unicode name of the window.
        


## -returns



Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a></b>

Stream that can be used to load or save the view state.



