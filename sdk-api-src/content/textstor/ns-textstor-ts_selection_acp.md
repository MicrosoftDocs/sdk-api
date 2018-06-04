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

# TS_SELECTION_ACP structure


## -description



The <b>TS_SELECTION_ACP</b> structure contains ACP-based text selection data.




## -struct-fields




### -field acpStart

Contains the start position of the selection.


### -field acpEnd

Contains the end position of the selection.


### -field style

A <a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE</a> structure that contains additional selection data.


## -see-also




<a href="https://msdn.microsoft.com/e2052daf-4168-4266-ae8d-a09ecbfeb422">ITextStoreACP::GetSelection
      </a>



<a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">
        ITextStoreACP::SetSelection
      </a>



<a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">
        TS_SELECTIONSTYLE
      </a>
 

 

