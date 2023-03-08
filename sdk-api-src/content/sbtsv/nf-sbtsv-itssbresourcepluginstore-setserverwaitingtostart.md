---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetServerWaitingToStart
title: ITsSbResourcePluginStore::SetServerWaitingToStart (sbtsv.h)
description: Indicates to the session host that the server is waiting to start.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetServerWaitingToStart method","ITsSbResourcePluginStore.SetServerWaitingToStart","ITsSbResourcePluginStore::SetServerWaitingToStart","SetServerWaitingToStart","SetServerWaitingToStart method [Remote Desktop Services]","SetServerWaitingToStart method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::SetServerWaitingToStart","termserv.itssbresourcepluginstore_setserverwaitingtostart"]
old-location: termserv\itssbresourcepluginstore_setserverwaitingtostart.htm
tech.root: TermServ
ms.assetid: cf677be1-387b-4a63-902b-bacda8729b23
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetServerWaitingToStart method, ITsSbResourcePluginStore.SetServerWaitingToStart, ITsSbResourcePluginStore::SetServerWaitingToStart, SetServerWaitingToStart, SetServerWaitingToStart method [Remote Desktop Services], SetServerWaitingToStart method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetServerWaitingToStart, termserv.itssbresourcepluginstore_setserverwaitingtostart
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbResourcePluginStore::SetServerWaitingToStart
 - sbtsv/ITsSbResourcePluginStore::SetServerWaitingToStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.SetServerWaitingToStart
---

# ITsSbResourcePluginStore::SetServerWaitingToStart


## -description

Indicates to the session host that the server is waiting to start.

## -parameters

### -param PoolName [in]

Name of the pool.

### -param serverName [in]

Name of the server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>