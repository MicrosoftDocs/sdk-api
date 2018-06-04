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

# INamespaceWalkCB2::WalkComplete


## -description


Removes data collected during a namespace walk.


## -parameters




### -param hr [in]

Type: <b>HRESULT</b>

The results of <a href="https://msdn.microsoft.com/cfe328f4-6db5-423b-b944-f0f390359793">Walk</a>.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



