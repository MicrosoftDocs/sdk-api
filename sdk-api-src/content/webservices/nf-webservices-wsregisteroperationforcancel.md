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

# WsRegisterOperationForCancel function


## -description



                A service operation can use this function to register for a cancel notification. 
                It is only valid to call this API when the service operation is executing. The behavior 
                for calling it after the completion of Service Operation is not supported.
            


                While this API is being called and the runtime has determined that the cancellation of the 
                service operation is necessary, it can call the callback during the call to this API by the application. 
            


                The caller should therefore assume that the runtime may call on the callback 
                <a href="https://msdn.microsoft.com/177f9abb-861d-42a9-8044-25076b026f1d">WS_OPERATION_CANCEL_CALLBACK</a> as soon as the WsRegisterOperationForCancel is called.
            


## -parameters




### -param context [in]

The context that the property value is being obtained for.


### -param cancelCallback [in]


                    Function pointer for cancel notification function.
                


### -param freestateCallback [in, optional]


                    A optional parameter specifying the function pointer to the free state call. 
                


### -param userState [in, optional]


                    A optional parameter specifying the application specific state which can be used to identify call data. 
                


### -param error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



