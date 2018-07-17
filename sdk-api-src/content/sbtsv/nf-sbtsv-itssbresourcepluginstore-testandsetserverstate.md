---
UID: NF:sbtsv.ITsSbResourcePluginStore.TestAndSetServerState
title: ITsSbResourcePluginStore::TestAndSetServerState
author: windows-sdk-content
description: Conditionally sets a new state on a server.
old-location: termserv\itssbresourcepluginstore_testandsetserverstate.htm
old-project: termserv
ms.assetid: 5b209587-090e-4338-95b3-542e50412587
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],TestAndSetServerState method, ITsSbResourcePluginStore.TestAndSetServerState, ITsSbResourcePluginStore::TestAndSetServerState, TestAndSetServerState, TestAndSetServerState method [Remote Desktop Services], TestAndSetServerState method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::TestAndSetServerState, termserv.itssbresourcepluginstore_testandsetserverstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.TestAndSetServerState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbResourcePluginStore::TestAndSetServerState


## -description


Conditionally sets a new state on a server. 


## -parameters




### -param PoolName [in]

Name of the pool.


### -param ServerFQDN [in]

Fully qualified domain name (FQDN) of the server.


### -param NewState [in]

The state to set.


### -param TestState [in]

If set to <b>TARGET_UNKNOWN</b> or the current state of the server, the  server will be set as specified in the <i>NewState</i> parameter.


### -param pInitState [out]

On return, points to the previous state of the server.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>
 

 

