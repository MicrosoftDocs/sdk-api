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

# WsFreeSecurityToken function


## -description


Releases the memory resource associated with  a <b>Security Token</b> object.
            


## -parameters




### -param token [in]

A pointer to the <b>Security Token</b> object to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/050a2ce5-279e-48fb-85da-1d0b11cd8229">WS_SECURITY_TOKEN</a>
object returned by <a href="https://msdn.microsoft.com/1d82c6c3-2bcf-4883-aed7-1a163bbb2228">WsCreateXmlSecurityToken</a>.
                


## -returns



This function does not return a value.



