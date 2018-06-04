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

# IBDA_ConditionalAccess::get_SmartCardStatus


## -description


The <b>get_SmartCardStatus</b> method retrieves the status of the smart card.


## -parameters




### -param pCardStatus [out]


            Pointer to a variable of type <a href="https://msdn.microsoft.com/c699c6a9-f554-4e2d-ac7f-9b5ff954fa6b">SmartCardStatusType</a> that receives the card status type.
          


### -param pCardAssociation [out]


            Pointer to a variable of type <a href="https://msdn.microsoft.com/42fe27ed-d461-43bf-87c5-bd0704339ec7">SmartCardAssociationType</a> that receives the card association type.
          


### -param pbstrCardError [out]


            Receives a string containing the card error. When the string is no longer required, call the <b>SysFreeString</b> function to free it.
          


### -param pfOOBLocked






## -returns




            If the method succeeds, it returns S_OK. If it fails, it returns an error code.
          




## -remarks



All three parameters must be non-NULL or the method fails and returns <b>E_POINTER</b>.




## -see-also




<a href="https://msdn.microsoft.com/93bd3c38-2591-4d36-b296-5ad939487277">IBDA_ConditionalAccess Interface</a>
 

 

