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

# WS_SERVICE_SECURITY_CALLBACK callback function


## -description



                Invoked when headers of the incoming message 
                are received and the body is not processed.
            


## -parameters




### -param *context [in]


                    The incoming message with headers only.
                


### -param *authorized [out]


                    Set to <b>TRUE</b>, if authorization succeeded, <b>FALSE</b> if authorization failed.
                


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails. 
                


## -returns



This callback function does not return a value.



