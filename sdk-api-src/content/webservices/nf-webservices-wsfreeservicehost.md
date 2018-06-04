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

# WsFreeServiceHost function


## -description


Releases the memory associated with  a <a href="https://msdn.microsoft.com/42e4d24d-5611-4561-b874-6dc3f3f88c73">Service Host</a> object.
            


## -parameters




### -param serviceHost [in]

A pointer to the <b>Service Host</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a> object
                    returned by <a href="https://msdn.microsoft.com/412a262a-1706-4101-b154-1804408a5b9f">WsCreateServiceHost</a> and the referenced <b>Service Host</b> value may not be <b>NULL</b>.
        
                


## -returns



This function does not return a value.



