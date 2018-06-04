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

# WS_PROXY_MESSAGE_CALLBACK callback function


## -description


Invoked when the headers of the input message are 
                about to be sent, or when output message headers are just received. 
            


## -parameters




### -param *message [in]


                    The input or output message.
                


### -param *heap [in]


                    The heap associated with the call. This is the heap which is passed to call for which this 
                    callback is being called.
                


### -param *state [in]


                    The 'state' as specified as part of <a href="https://msdn.microsoft.com/1dfde962-7475-430a-b586-1684a173908f">WS_PROXY_MESSAGE_CALLBACK_CONTEXT</a> 'state' field.
                


### -param *error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




                See also, <a href="https://msdn.microsoft.com/1dfde962-7475-430a-b586-1684a173908f">WS_PROXY_MESSAGE_CALLBACK_CONTEXT</a>.
            



