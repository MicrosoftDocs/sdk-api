---
UID: NF:sbtsv.ITsSbResourcePluginStore.EnumerateSessions
title: ITsSbResourcePluginStore::EnumerateSessions
author: windows-driver-content
description: Enumerates a specified set of sessions.
old-location: termserv\itssbresourcepluginstore_enumeratesessions.htm
old-project: TermServ
ms.assetid: 217b5c28-b0f8-4a8f-8695-8c8e0895b508
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: EnumerateSessions, EnumerateSessions method [Remote Desktop Services], EnumerateSessions method [Remote Desktop Services],ITsSbResourcePluginStore interface, EnumerateSessions method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],EnumerateSessions method, ITsSbResourcePluginStore.EnumerateSessions, ITsSbResourcePluginStore::EnumerateSessions, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],EnumerateSessions method, ITsSbResourcePluginStoreEx::EnumerateSessions, sbtsv/ITsSbResourcePluginStore::EnumerateSessions, sbtsv/ITsSbResourcePluginStoreEx::EnumerateSessions, termserv.itssbresourcepluginstore_enumeratesessions
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
-	ITsSbResourcePluginStore.EnumerateSessions
-	ITsSbResourcePluginStoreEx.EnumerateSessions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbResourcePluginStore::EnumerateSessions


## -description


Enumerates a specified set of sessions.


## -parameters




### -param targetName [in]

The name of the target.


### -param userName [in]

The name of the user account.


### -param userDomain [in]

The domain name of the user account.


### -param poolName [in]

The name of the pool.


### -param initialProgram [in]

The name of the published remote application.


### -param pSessionState [in]

A pointer to the  <a href="https://msdn.microsoft.com/2780e704-72f1-44a9-ad54-ab3d2b19befe">TSSESSION_STATE</a> value of the sessions to enumerate.


### -param pdwCount [in, out]

Returns a pointer to the number of sessions returned.


### -param ppVal [out]

Returns the list of sessions requested.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

