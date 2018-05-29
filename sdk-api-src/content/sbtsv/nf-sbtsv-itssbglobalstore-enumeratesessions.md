---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateSessions
title: ITsSbGlobalStore::EnumerateSessions
author: windows-sdk-content
description: Returns an array that contains sessions on the specified provider.
old-location: termserv\itssbglobalstore_enumeratesessions.htm
old-project: TermServ
ms.assetid: 16fe9154-913a-4b7f-8ab5-ea8654b7cc98
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: EnumerateSessions, EnumerateSessions method [Remote Desktop Services], EnumerateSessions method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateSessions method, ITsSbGlobalStore.EnumerateSessions, ITsSbGlobalStore::EnumerateSessions, sbtsv/ITsSbGlobalStore::EnumerateSessions, termserv.itssbglobalstore_enumeratesessions
ms.prod: windows
ms.technology: windows-sdk
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
-	ITsSbGlobalStore.EnumerateSessions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbGlobalStore::EnumerateSessions


## -description


Returns an array that contains sessions on the specified provider.


## -parameters




### -param ProviderName [in]

The name of the provider.


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




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

