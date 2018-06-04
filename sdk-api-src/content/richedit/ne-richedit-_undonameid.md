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

# _undonameid enumeration


## -description


Contains values that indicate types of rich edit control actions that can be undone or redone. The <a href="https://msdn.microsoft.com/8649236f-32dc-45d3-847e-c9f65ffba44c">EM_GETREDONAME</a> and <a href="https://msdn.microsoft.com/43351909-f8bc-425a-9d9b-655e3b47eb75">EM_GETUNDONAME</a> messages use this enumeration type to return a value. 


## -enum-fields




### -field UID_UNKNOWN

The type of undo action is unknown. 


### -field UID_TYPING

Typing operation. 


### -field UID_DELETE

Delete operation. 


### -field UID_DRAGDROP

Drag-and-drop operation. 


### -field UID_CUT

Cut operation. 


### -field UID_PASTE

Paste operation. 


### -field UID_AUTOTABLE

Automatic table insertion; for example, typing +---+---+&lt;Enter&gt; to insert a table row. 



## -see-also




<a href="https://msdn.microsoft.com/8649236f-32dc-45d3-847e-c9f65ffba44c">EM_GETREDONAME</a>



<a href="https://msdn.microsoft.com/43351909-f8bc-425a-9d9b-655e3b47eb75">EM_GETUNDONAME</a>



<b>Reference</b>
 

 

