---
UID: NF:sbtsv.ITsSbResourcePluginStore.AddSessionToStore
title: ITsSbResourcePluginStore::AddSessionToStore
author: windows-sdk-content
description: Adds a new session to the resource plug-in store.
old-location: termserv\itssbresourcepluginstore_addsessiontostore.htm
tech.root: termserv
ms.assetid: 354ca945-cefe-42f6-a255-9918b8ffc339
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddSessionToStore, AddSessionToStore method [Remote Desktop Services], AddSessionToStore method [Remote Desktop Services],ITsSbResourcePluginStore interface, AddSessionToStore method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],AddSessionToStore method, ITsSbResourcePluginStore.AddSessionToStore, ITsSbResourcePluginStore::AddSessionToStore, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],AddSessionToStore method, ITsSbResourcePluginStoreEx::AddSessionToStore, sbtsv/ITsSbResourcePluginStore::AddSessionToStore, sbtsv/ITsSbResourcePluginStoreEx::AddSessionToStore, termserv.itssbresourcepluginstore_addsessiontostore
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
 - ITsSbResourcePluginStore.AddSessionToStore
 - ITsSbResourcePluginStoreEx.AddSessionToStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourcePluginStore::AddSessionToStore


## -description


Adds a new session to the resource plug-in store. Call this method when a user has logged on to a new session.


## -parameters




### -param pSession [in]

A pointer to an <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> session object. The target name, user name, domain name, and session ID are required fields.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>



<a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a>
 

 

