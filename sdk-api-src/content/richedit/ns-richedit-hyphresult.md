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

# hyphresult structure


## -description


Contains information about the result of hyphenation in a Microsoft Rich Edit control.
		


## -struct-fields




### -field khyph

Type: <b><a href="https://msdn.microsoft.com/900cae36-d2e3-4a30-97ca-1cc832fd2687">KHYPH</a></b>


            The type of hyphenation. 


### -field ichHyph

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The index of the WCHAR in the passed string where hyphenation occurred. 


### -field chHyph

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WCHAR</a></b>

The character used when hyphenation requires a replacement or an addition or a change. If no new character is needed, the value is zero. 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/2463189e-98cf-4545-a435-474df74e1a22">HYPHENATEINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/2463189e-98cf-4545-a435-474df74e1a22">HYPHENATEINFO</a>



<a href="https://msdn.microsoft.com/900cae36-d2e3-4a30-97ca-1cc832fd2687">KHYPH</a>



<b>Reference</b>
 

 

