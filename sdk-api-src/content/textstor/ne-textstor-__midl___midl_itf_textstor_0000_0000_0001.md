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

# __MIDL___MIDL_itf_textstor_0000_0000_0001 enumeration


## -description


Elements of the <b>TsActiveSelEnd</b> enumeration specify which end of a text store selection is active.


## -enum-fields




### -field TS_AE_NONE

The selection has no active end. This is typical for all selections other than the default selection.


### -field TS_AE_START

The active end of the selection is at the start of the range of text.


### -field TS_AE_END

The active end of the selection is at the end of the range of text.


## -remarks



The active end of a selection is the end likely to respond to user actions. For example, in many applications, holding down the SHIFT key while using the arrow keys will change the selection. The end of the selection that moves is the active end of the selection.

This enumeration is used in the <a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE
      </a>
 

 

