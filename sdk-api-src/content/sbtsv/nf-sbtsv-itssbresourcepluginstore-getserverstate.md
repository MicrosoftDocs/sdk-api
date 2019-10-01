---
UID: NF:sbtsv.ITsSbResourcePluginStore.GetServerState
title: ITsSbResourcePluginStore::GetServerState (sbtsv.h)
author: windows-sdk-content
description: Retrieves the state of a specified server.
old-location: termserv\itssbresourcepluginstore_getserverstate.htm
tech.root: TermServ
ms.assetid: 287863fe-55b3-456e-9488-09ee85af2e15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetServerState, GetServerState method [Remote Desktop Services], GetServerState method [Remote Desktop Services],ITsSbResourcePluginStore interface, ITsSbResourcePluginStore interface [Remote Desktop Services],GetServerState method, ITsSbResourcePluginStore.GetServerState, ITsSbResourcePluginStore::GetServerState, sbtsv/ITsSbResourcePluginStore::GetServerState, termserv.itssbresourcepluginstore_getserverstate
ms.topic: method
f1_keywords: 
 - "sbtsv/ITsSbResourcePluginStore.GetServerState"
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
 - ITsSbResourcePluginStore.GetServerState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourcePluginStore::GetServerState


## -description


Retrieves the state of a specified server.


## -parameters




### -param PoolName [in]

Name of the pool.


### -param ServerFQDN [in]

Fully qualified domain name (FQDN) of the server.


### -param pState [out]

On return, points to the state of the server.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>
 

 

