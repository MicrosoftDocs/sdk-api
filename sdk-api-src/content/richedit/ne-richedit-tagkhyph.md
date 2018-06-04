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

# tagKHYPH enumeration


## -description


Contains values used to specify how to do hyphenation in a rich edit control. The <a href="https://msdn.microsoft.com/5a7333ab-4918-4d73-9ad5-a8704acab4c0">HyphenateProc</a> callback function uses this enumeration type. 


## -enum-fields




### -field khyphNil

No hyphenation is allowed. 


### -field khyphNormal

Do not change any characters during hyphenation.


### -field khyphAddBefore

Add a letter before the hyphenation mark. 


### -field khyphChangeBefore

Change the letter before the hyphenation mark. 


### -field khyphDeleteBefore

Delete the letter before the hyphenation mark. 


### -field khyphChangeAfter

Change the letter after the hyphenation mark. 


### -field khyphDelAndChange

The two letters before the hyphenation mark are replaced by one character; see the <b>chHyph</b> member of <a href="https://msdn.microsoft.com/43b9d78f-5931-49bd-8c58-cc333a3f3756">HYPHRESULT</a>.


## -remarks



Hyphenation rules are specific for each language; not all hyphenation types are valid for a given language.




## -see-also




<a href="https://msdn.microsoft.com/43b9d78f-5931-49bd-8c58-cc333a3f3756">HYPHRESULT</a>



<a href="https://msdn.microsoft.com/5a7333ab-4918-4d73-9ad5-a8704acab4c0">HyphenateProc</a>



<b>Reference</b>
 

 

