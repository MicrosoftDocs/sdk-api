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

# WsFreeMetadata function


## -description



                Releases the memory resource associated with a metadata object.
            


## -parameters




### -param metadata [in]


                    
                    A pointer to the metadata object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/aa7383a1-60fa-448a-b0c6-b9c49d9d5070">WS_METADATA</a> object returned
                    by <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> and the referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.




## -remarks




                Any <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> objects that
                were retrieved using the metadata object will also be freed.
            



