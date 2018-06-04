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

# TF_SELECTIONSTYLE structure


## -description



The <b>TF_SELECTIONSTYLE</b> structure represents the style of a selection.




## -struct-fields




### -field ase

Specifies the active end of the selection. For more information, see <a href="https://msdn.microsoft.com/bb89f0b4-a0b4-42ea-8467-6fc634e37aec">TfActiveSelEnd</a>.


### -field fInterimChar

Indicates if the selection is an interim character. If this value is nonzero, then the seleciton is an interim character and <b>ase</b> will be TF_AE_NONE. If this value is zero, the selection is not an interim character.


## -remarks



An interim character selection spans exactly one character and is visually represented as a solid rectangle that is usually flashing. This is a standard UI element of Korean and some Chinese character compositions. <b>fInterimChar</b> is an indication that a specific character is composed. <b>fInterimChar</b> can only be nonzero for a single selection. In this case, there will be no caret because the highlight replaces it.




## -see-also




<a href="https://msdn.microsoft.com/c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54">
        TF_SELECTION
      </a>



<a href="https://msdn.microsoft.com/bb89f0b4-a0b4-42ea-8467-6fc634e37aec">TfActiveSelEnd
      </a>
 

 

