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

# TS_SELECTIONSTYLE structure


## -description



The <b>TS_SELECTIONSTYLE</b> structure represents the style of a selection.




## -struct-fields




### -field ase

Specifies the active end of the selection. For more information, see <a href="https://msdn.microsoft.com/95695f10-2296-41fe-b2b4-efae548292bb">TsActiveSelEnd</a>.


### -field fInterimChar

Indicates if the selection is an interim character. If this value is nonzero, then the seleciton is an interim character and <b>ase</b> will be TS_AE_NONE. If this value is zero, the selection is not an interim character.


## -remarks



An interim character selection is the length of one character and is visually represented as a solid rectangle that is usually flashing. This is a standard UI element of Korean and some Chinese character compositions. <b>fInterimChar</b> is an indication that a specific character is being composed. <b>fInterimChar</b> can only be nonzero for a single selection. In this case, there will be no caret because the highlight takes its place.




## -see-also




<a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">
        TS_SELECTION_ACP
      </a>



<a href="https://msdn.microsoft.com/56fbe145-1972-4b44-a730-17860e428dd0">
        TS_SELECTION_ANCHOR
      </a>



<a href="https://msdn.microsoft.com/95695f10-2296-41fe-b2b4-efae548292bb">TsActiveSelEnd
      </a>
 

 

