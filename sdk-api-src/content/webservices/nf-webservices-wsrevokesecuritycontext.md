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

# WsRevokeSecurityContext function


## -description



        Revokes a security context. Can only be called on the server side. 
        Further requests using this security context will fail and a fault will be sent to the client.
      


        This function can be used when the server knows that no more messages are 
        coming and does not want to wait for the client or the context timeouts to 
        trigger the reclaiming of resources, or when the server wants to engage in 
        active context management.
      


## -parameters




### -param securityContext [in]


          The security context to be revoked.
        


### -param error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



