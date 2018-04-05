---
UID: NF:sbtsv.ITsSbResourcePluginStore.QuerySessionBySessionId
title: ITsSbResourcePluginStore::QuerySessionBySessionId method
author: windows-driver-content
description: Returns the session object that has the specified session ID.
old-location: termserv\itssbresourcepluginstore_querysessionbysessionid.htm
old-project: TermServ
ms.assetid: 51a1e876-09fb-4b1c-bb86-028afc46f31e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ITsSbResourcePluginStore, ITsSbResourcePluginStore interface [Remote Desktop Services], QuerySessionBySessionId method, ITsSbResourcePluginStore::QuerySessionBySessionId, ITsSbResourcePluginStoreEx interface [Remote Desktop Services], QuerySessionBySessionId method, ITsSbResourcePluginStoreEx::QuerySessionBySessionId, QuerySessionBySessionId method [Remote Desktop Services], QuerySessionBySessionId method [Remote Desktop Services], ITsSbResourcePluginStore interface, QuerySessionBySessionId method [Remote Desktop Services], ITsSbResourcePluginStoreEx interface, QuerySessionBySessionId,ITsSbResourcePluginStore.QuerySessionBySessionId, sbtsv/ITsSbResourcePluginStore::QuerySessionBySessionId, sbtsv/ITsSbResourcePluginStoreEx::QuerySessionBySessionId, termserv.itssbresourcepluginstore_querysessionbysessionid
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbResourcePluginStore.QuerySessionBySessionId
-	ITsSbResourcePluginStoreEx.QuerySessionBySessionId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITsSbResourcePluginStore::QuerySessionBySessionId method


## -description


Returns the session object that has the specified session ID.


## -parameters




### -param dwSessionId [in]

The session ID.


### -param TargetName [in]

The target name.


### -param ppSession [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> session object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A resource plug-in can use this method to retrieve a session object. Unlike the global store, the resource plug-in store does not copy the session object retrieved because the resource plug-in owns the session object.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>



<a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a>
 

 

