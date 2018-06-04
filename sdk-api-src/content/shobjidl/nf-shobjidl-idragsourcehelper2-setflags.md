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

# IDragSourceHelper2::SetFlags


## -description


Sets the characteristics of a drag-and-drop operation over an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

The flags that determine the characteristics of a drag-and-drop operation over an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object.



#### DSH_ALLOWDROPDESCRIPTIONTEXT (0x0001)

Allow text specified in <a href="https://msdn.microsoft.com/78757001-cac8-412d-a6c3-74bae6eb3ad8">DROPDESCRIPTION</a> to be displayed on the drag image. If you pass this flag into the <i>dwFlags</i> parameter of <b>IDragSourceHelper2::SetFlags</b>, then the text description is rendered on top of the supplied drag image. If you pass a drag image into an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object, then by default, the extra text description of the drag-and-drop operation is not displayed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



