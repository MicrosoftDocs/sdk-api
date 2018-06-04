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

# IMenuPopup::SetSubMenu


## -description


Sets the given menu bar interface to be the submenu of the calling application object's interface.


## -parameters




### -param pmp [in]

Type: <b><a href="https://msdn.microsoft.com/dc5749b1-43b7-4f68-ac38-8a6e99613149">IMenuPopup</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/dc5749b1-43b7-4f68-ac38-8a6e99613149">IMenuPopup</a> interface that specifies the menu bar of interest.


### -param fSet

Type: <b>BOOL</b>

Removes the submenu if <i>fSet</i> is set to <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



