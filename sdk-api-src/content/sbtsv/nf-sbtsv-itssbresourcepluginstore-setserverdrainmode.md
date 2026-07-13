---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetServerDrainMode
title: ITsSbResourcePluginStore::SetServerDrainMode (sbtsv.h)
description: Sets the drain mode of the specified server.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetServerDrainMode method","ITsSbResourcePluginStore.SetServerDrainMode","ITsSbResourcePluginStore::SetServerDrainMode","SetServerDrainMode","SetServerDrainMode method [Remote Desktop Services]","SetServerDrainMode method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::SetServerDrainMode","termserv.itssbresourcepluginstore_setserverdrainmode"]
old-location: termserv\itssbresourcepluginstore_setserverdrainmode.htm
tech.root: TermServ
ms.assetid: E0213889-7CC9-446A-9EFF-7C8B02E4A35D
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetServerDrainMode method, ITsSbResourcePluginStore.SetServerDrainMode, ITsSbResourcePluginStore::SetServerDrainMode, SetServerDrainMode, SetServerDrainMode method [Remote Desktop Services], SetServerDrainMode method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetServerDrainMode, termserv.itssbresourcepluginstore_setserverdrainmode
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
 - ITsSbResourcePluginStore::SetServerDrainMode
 - sbtsv/ITsSbResourcePluginStore::SetServerDrainMode
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
 - ITsSbResourcePluginStore.SetServerDrainMode
---

# ITsSbResourcePluginStore::SetServerDrainMode


## -description

Sets the drain mode of the specified server.

## -parameters

### -param ServerFQDN [in]

The fully qualified domain name of the server.

### -param DrainMode [in]

The mode to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>