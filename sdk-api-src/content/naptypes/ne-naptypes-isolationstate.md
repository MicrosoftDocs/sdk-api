---
UID: NE:naptypes.tagIsolationState
title: IsolationState (naptypes.h)
description: Describes the isolation state of a connection.
helpviewer_keywords: ["IsolationState","IsolationState enumeration [NAP]","isolationStateInProbation","isolationStateNotRestricted","isolationStateRestrictedAccess","nap.isolationstate_enum","naptypes/IsolationState","naptypes/isolationStateInProbation","naptypes/isolationStateNotRestricted","naptypes/isolationStateRestrictedAccess"]
old-location: nap\isolationstate_enum.htm
tech.root: NAP
ms.assetid: 79f81e8e-a105-4cc9-b175-8a364648f3a6
ms.date: 12/05/2018
ms.keywords: IsolationState, IsolationState enumeration [NAP], isolationStateInProbation, isolationStateNotRestricted, isolationStateRestrictedAccess, nap.isolationstate_enum, naptypes/IsolationState, naptypes/isolationStateInProbation, naptypes/isolationStateNotRestricted, naptypes/isolationStateRestrictedAccess
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IsolationState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIsolationState
 - naptypes/tagIsolationState
 - IsolationState
 - naptypes/IsolationState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - IsolationState
---

# IsolationState enumeration


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>IsolationState</b> enumeration  describes the isolation state of a connection.

## -enum-fields

### -field isolationStateNotRestricted:1

The connection isolation state is not restricted.

### -field isolationStateInProbation:2

The connection isolation state is probation.

### -field isolationStateRestrictedAccess:3

The connection isolation state is restricted access.

