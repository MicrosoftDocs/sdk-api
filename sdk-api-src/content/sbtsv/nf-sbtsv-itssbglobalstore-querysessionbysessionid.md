---
UID: NF:sbtsv.ITsSbGlobalStore.QuerySessionBySessionId
title: ITsSbGlobalStore::QuerySessionBySessionId
author: windows-sdk-content
description: Retrieves the ITsSbSession object associated with the given session ID.
old-location: termserv\itssbglobalstore_querysessionbysessionid.htm
tech.root: termserv
ms.assetid: d710842a-9bd5-4791-8f6e-bac2fe07c93f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITsSbGlobalStore interface [Remote Desktop Services],QuerySessionBySessionId method, ITsSbGlobalStore.QuerySessionBySessionId, ITsSbGlobalStore::QuerySessionBySessionId, QuerySessionBySessionId, QuerySessionBySessionId method [Remote Desktop Services], QuerySessionBySessionId method [Remote Desktop Services],ITsSbGlobalStore interface, sbtsv/ITsSbGlobalStore::QuerySessionBySessionId, termserv.itssbglobalstore_querysessionbysessionid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGlobalStore.QuerySessionBySessionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbGlobalStore::QuerySessionBySessionId


## -description


Retrieves the <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> object associated with the given 
session ID.


## -parameters




### -param ProviderName [in]

The resource plug-in provider name that owns the target.


### -param dwSessionId [in]

The session ID.


### -param TargetName [in]

The name of the target computer on which this session is present.


### -param ppSession [out]

A pointer to a pointer to a session object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



This method can return one of these values.




## -remarks



Any changes made to the target objects returned by this method do not affect the target objects stored 
in Remote Desktop Connection Broker (RD Connection Broker). The target objects returned are copies of the target objects in RD Connection Broker.




## -see-also




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

