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

# IFolderViewOptions::GetFolderViewOptions


## -description


Retrieves the current set of options for the view.


## -parameters




### -param pfvoFlags [out]

Type: <b><a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a>*</b>

A bitmask that, when this method returns successfully, receives the <a href="https://msdn.microsoft.com/ab0ebc82-e917-4e3a-864b-fc3bb6280a48">FOLDERVIEWOPTIONS</a> values that are currently set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



