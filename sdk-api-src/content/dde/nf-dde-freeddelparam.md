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

# FreeDDElParam function


## -description


Frees the memory specified by the 
			<i>lParam</i> parameter of a posted Dynamic Data Exchange (DDE) message. An application receiving a posted DDE message should call this function after it has used the <a href="https://msdn.microsoft.com/a7da276f-0e29-4abc-86cf-ac1fd23d84b0">UnpackDDElParam</a> function to unpack the 
			<i>lParam</i> value. 


## -parameters




### -param msg [in]

Type: <b>UINT</b>

The posted DDE message. 


### -param lParam [in]

Type: <b>LPARAM</b>

The 
					<i>lParam</i> parameter of the posted DDE message. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks



An application should call this function only for posted DDE messages. 

This function frees the memory specified by the 
				<i>lParam</i> parameter. It does not free the contents of 
				<i>lParam</i>. 




## -see-also




<a href="https://msdn.microsoft.com/0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9131229d-2515-40d2-a4a8-4c8f7987ac09">PackDDElParam</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/069ac8ee-3d92-4969-8c6b-78a8a0c76721">ReuseDDElParam</a>



<a href="https://msdn.microsoft.com/a7da276f-0e29-4abc-86cf-ac1fd23d84b0">UnpackDDElParam</a>
 

 

