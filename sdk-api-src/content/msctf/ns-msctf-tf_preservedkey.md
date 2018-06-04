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

# TF_PRESERVEDKEY structure


## -description



The <b>TF_PRESERVEDKEY</b> structure represents a preserved key.




## -struct-fields




### -field uVKey

Virtual key code of the keyboard shortcut.


### -field uModifiers

Modifies the preserved key. This can be zero or a combination of one or more of the <a href="https://msdn.microsoft.com/4642ef17-34bd-4482-a9e9-0fbed7b574b1">TF_MOD_* constants</a>.


## -remarks



Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://msdn.microsoft.com/4642ef17-34bd-4482-a9e9-0fbed7b574b1">TF_MOD_* constants
      </a>
 

 

