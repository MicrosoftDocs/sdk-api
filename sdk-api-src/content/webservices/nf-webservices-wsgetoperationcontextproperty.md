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

# WsGetOperationContextProperty function


## -description



                Returns a property of the specified operation context. It should be noted that the 
                validity of these property is limited to the lifetime of the operation context itself. 
                


## -parameters




### -param context [in]

The context that the property value is being obtained for.


### -param id [in]


                    The id of the property.
                


### -param value


                    The address to place the retrieved value. The contents are not modified in case of a failure.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]


                    The size of the buffer that the caller has allocated for the retrieved value.
                


### -param error [in, optional]


                    Specifies where additional error information should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



