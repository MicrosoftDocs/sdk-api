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

# tagHyphenateInfo structure


## -description


Contains information about hyphenation in a Microsoft Rich Edit control.
		


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Size of the <b>HYPHENATEINFO</b> structure, in bytes. 


### -field dxHyphenateZone

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SHORT</a></b>

Size, in TWIPS (one TWIP is 1/1440 inch), of the area near the margin that excludes hyphenation. If a space character is closer to the margin than this value, do not hyphenate the following word. 


### -field pfnHyphenate

Type: <b>PFNHYPHENATEPROC</b>

The client-defined <a href="https://msdn.microsoft.com/5a7333ab-4918-4d73-9ad5-a8704acab4c0">HyphenateProc</a> callback function. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/70ccb698-e440-493b-8f38-2bf7f32e4b26">EM_GETHYPHENATEINFO</a> and <a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a> messages.




## -see-also




<a href="https://msdn.microsoft.com/70ccb698-e440-493b-8f38-2bf7f32e4b26">EM_GETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/67126cb8-ab50-49a9-b32f-2245debf2fe3">EM_SETHYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/5a7333ab-4918-4d73-9ad5-a8704acab4c0">HyphenateProc</a>



<b>Reference</b>
 

 

