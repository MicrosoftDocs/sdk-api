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

# _findtextexw structure


## -description


Contains information about text to search for in a rich edit control. This structure is used with the <a href="https://msdn.microsoft.com/f1bf925b-2776-40b8-9d05-8484daf8d989">EM_FINDTEXTEX</a> message.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters to search. To search forward in the entire control, set <b>cpMin</b> to 0 and <b>cpMax</b> to -1. 


### -field lpstrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The null-terminated string to find. 


### -field chrgText

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters in which the text was found. If the text was not found, <b>cpMin</b> and <b>cpMax</b> are -1.


## -see-also




<a href="https://msdn.microsoft.com/f1bf925b-2776-40b8-9d05-8484daf8d989">EM_FINDTEXTEX</a>



<a href="https://msdn.microsoft.com/7b90ef06-0395-430e-8b5d-b392481a5f70">EM_FINDTEXTEXW</a>



<b>Reference</b>
 

 

