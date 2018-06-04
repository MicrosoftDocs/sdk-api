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

# _charrange structure


## -description



	 Specifies a range of characters in a rich edit control.

If the <b>cpMin</b> and <b>cpMax</b> members are equal, the range is empty. The range includes everything if <b>cpMin</b> is 0 and <b>cpMax</b> is –1.


## -struct-fields




### -field cpMin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character position index immediately preceding the first character in the range. 


### -field cpMax

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character position immediately following the last character in the range. 


## -see-also




<a href="https://msdn.microsoft.com/60fcf13e-6c45-4f4e-9b54-70f0985122fb">EM_EXGETSEL</a>



<a href="https://msdn.microsoft.com/85a0d1d4-1826-4ac5-b823-de81a051441d">EM_EXSETSEL</a>



<b>Reference</b>
 

 

