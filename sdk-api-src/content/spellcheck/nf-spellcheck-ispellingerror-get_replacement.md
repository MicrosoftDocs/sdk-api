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

# ISpellingError::get_Replacement


## -description


Gets the text to use as replacement text when the corrective action is replace.

This property is read-only.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/370CF89E-97BF-4AB5-8AD6-3B2DF08463E0">CORRECTIVE_ACTION</a> returned by <a href="https://msdn.microsoft.com/9b28d194-01a3-4ea2-8428-d2e91e6abad8">CorrectiveAction</a> is not <b>CORRECTIVE_ACTION_REPLACE</b>, <i>value</i> is the empty string.




## -see-also




<a href="https://msdn.microsoft.com/370CF89E-97BF-4AB5-8AD6-3B2DF08463E0">CORRECTIVE_ACTION</a>



<a href="https://msdn.microsoft.com/9b28d194-01a3-4ea2-8428-d2e91e6abad8">CorrectiveAction</a>



<a href="https://msdn.microsoft.com/90a233a4-44a4-4f8f-92bb-ea65fa213616">ISpellingError</a>
 

 

