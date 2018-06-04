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

# WS_OPERATION_CANCEL_CALLBACK callback function


## -description


Gives notification of the cancellation of an 
                asynchronous service operation call as a result of an aborted shutdown of service host. 
             This callback is invoked by service model.


## -parameters




### -param reason [in]


                    Specifies the reason for which the call back is called.
                


### -param *state [in]


                    A reference to the application defined state registered with the callback. 
                


## -returns



This callback function does not return a value.




## -remarks




                See <a href="https://msdn.microsoft.com/3e456814-f70f-47ab-b866-f0b73d5cd35e">WsRegisterOperationForCancel</a> for details.
            



