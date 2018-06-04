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

# UnpackDDElParam function


## -description


Unpacks a Dynamic Data Exchange (DDE)<i>lParam</i> value received from a posted DDE message. 


## -parameters




### -param msg [in]

Type: <b>UINT</b>

The posted DDE message. 


### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message that was received. The application must free the memory object specified by the 
					<i>lParam</i> parameter by calling the <a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a> function. 


### -param puiLo [out]

Type: <b>PUINT_PTR</b>

A pointer to a variable that receives the low-order word of 
					<i>lParam</i>. 


### -param puiHi [out]

Type: <b>PUINT_PTR</b>

A pointer to a variable that receives the high-order word of 
					<i>lParam</i>. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks




<a href="https://msdn.microsoft.com/9131229d-2515-40d2-a4a8-4c8f7987ac09">PackDDElParam</a> eases the porting of 16-bit DDE applications to 32-bit DDE applications. 




## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/166cd1ed-2885-4275-8d92-76ae5344dd92">FreeDDElParam</a>



<a href="https://msdn.microsoft.com/9131229d-2515-40d2-a4a8-4c8f7987ac09">PackDDElParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/069ac8ee-3d92-4969-8c6b-78a8a0c76721">ReuseDDElParam</a>
 

 

