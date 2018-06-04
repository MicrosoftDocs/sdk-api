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

# WsFreeChannel function


## -description


Releases the memory resource associated with a Channel object.
            
                The <b>Channel</b> must be in the either the <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_CREATED</a> 
                or <b>WS_CHANNEL_STATE_CLOSED</b> state to be released.
            If a Channel has been successfully opened it must be closed before it
                can be released.
            


## -parameters




### -param channel [in]


          A pointer to the <b>Channel</b> object to release. The pointer must reference a valid <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> object returned
                    by <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a> or <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                    The referenced value may not be <b>NULL</b>.


## -returns



This function does not return a value.




## -remarks




                A channel that is in the process of being accepted/opened cannot be
                released until the accept/open completes.  Use <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a> to cancel the accept/open process.
            



