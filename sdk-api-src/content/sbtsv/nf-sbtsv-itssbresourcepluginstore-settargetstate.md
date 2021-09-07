---
UID: NF:sbtsv.ITsSbResourcePluginStore.SetTargetState
title: ITsSbResourcePluginStore::SetTargetState (sbtsv.h)
description: Sets the state of a target object.
helpviewer_keywords: ["ITsSbResourcePluginStore interface [Remote Desktop Services]","SetTargetState method","ITsSbResourcePluginStore.SetTargetState","ITsSbResourcePluginStore::SetTargetState","SetTargetState","SetTargetState method [Remote Desktop Services]","SetTargetState method [Remote Desktop Services]","ITsSbResourcePluginStore interface","sbtsv/ITsSbResourcePluginStore::SetTargetState","termserv.itssbresourcepluginstore_settargetstate"]
old-location: termserv\itssbresourcepluginstore_settargetstate.htm
tech.root: TermServ
ms.assetid: 5ba5c4c6-b644-45f7-8942-ee8ea543138d
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore interface [Remote Desktop Services],SetTargetState method, ITsSbResourcePluginStore.SetTargetState, ITsSbResourcePluginStore::SetTargetState, SetTargetState, SetTargetState method [Remote Desktop Services], SetTargetState method [Remote Desktop Services],ITsSbResourcePluginStore interface, sbtsv/ITsSbResourcePluginStore::SetTargetState, termserv.itssbresourcepluginstore_settargetstate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbResourcePluginStore::SetTargetState
 - sbtsv/ITsSbResourcePluginStore::SetTargetState
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
 - ITsSbResourcePluginStore.SetTargetState
---

# ITsSbResourcePluginStore::SetTargetState


## -description

Sets the state of a target object.

## -parameters

### -param targetName [in]

The name of the target.

### -param newState [in]

The <a href="/windows/desktop/api/sessdirpublictypes/ne-sessdirpublictypes-target_state">TARGET_STATE</a> value to set.

### -param pOldState [out]

The previous state of the target.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>