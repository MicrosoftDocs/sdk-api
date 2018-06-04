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

# _punctuation structure


## -description


Contains information about the punctuation used in a rich edit control.


## -struct-fields




### -field iSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of buffer pointed to by the 
					<b>szPunctuation</b> member, in bytes. 


### -field szPunctuation

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

The buffer containing the punctuation characters. 


## -remarks



This structure is used only in Asian-language versions of the operating system.




## -see-also




<a href="https://msdn.microsoft.com/1c04967b-d75e-4f54-b35b-cd50bac9cdfa">EM_GETPUNCTUATION</a>



<a href="https://msdn.microsoft.com/c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522">EM_SETPUNCTUATION</a>



<b>Reference</b>
 

 

