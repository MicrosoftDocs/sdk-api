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

# _tagSL_NONGENUINE_UI_OPTIONS structure


## -description


Specifies an application that displays a dialog box when the <a href="https://msdn.microsoft.com/e1983777-13c1-4bf5-834d-471db3bfa0f6">SLIsGenuineLocal</a> function indicates that an installation is not genuine.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pComponentId

A pointer to an <b>SLID</b> structure that specifies an application that displays a dialog box.


### -field hResultUI

The return value that the <a href="https://msdn.microsoft.com/e1983777-13c1-4bf5-834d-471db3bfa0f6">SLIsGenuineLocal</a> function returns when an installation is not genuine.

