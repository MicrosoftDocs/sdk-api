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

# __MIDL_ITfContext_0001 enumeration


## -description


Elements of the <b>TfActiveSelEnd</b> enumeration specify which end of a selected range of text is active.


## -enum-fields




### -field TF_AE_NONE

The selected range has no active end. This is typical for selected ranges other than the default selected range.


### -field TF_AE_START

The active end is at the start of the selected range.


### -field TF_AE_END

The active end is at the end of the selected range.


## -remarks



The active end of a selected range is the end likely to respond to user actions. For example, in many applications, holding the SHIFT key down while using the arrow keys will change the selected range. The end of the selected range that moves is the active end of the selected range.

This enumeration is used in the <a href="https://msdn.microsoft.com/3a38172b-611b-445f-be24-ea2a19178255">TF_SELECTIONSTYLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/3a38172b-611b-445f-be24-ea2a19178255">TF_SELECTIONSTYLE
      </a>
 

 

