---
UID: NE:naptypes.tagFixupState
title: FixupState (naptypes.h)
description: Defines the fix-up state of the System Health Agent (SHA).
helpviewer_keywords: ["FixupState","FixupState enumeration [NAP]","fixupStateCouldNotUpdate","fixupStateInProgress","fixupStateSuccess","nap.fixupstate_enum","naptypes/FixupState","naptypes/fixupStateCouldNotUpdate","naptypes/fixupStateInProgress","naptypes/fixupStateSuccess"]
old-location: nap\fixupstate_enum.htm
tech.root: NAP
ms.assetid: cde1f9df-f4d9-4601-a513-e00639ee9b6e
ms.date: 12/05/2018
ms.keywords: FixupState, FixupState enumeration [NAP], fixupStateCouldNotUpdate, fixupStateInProgress, fixupStateSuccess, nap.fixupstate_enum, naptypes/FixupState, naptypes/fixupStateCouldNotUpdate, naptypes/fixupStateInProgress, naptypes/fixupStateSuccess
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
req.typenames: FixupState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFixupState
 - naptypes/tagFixupState
 - FixupState
 - naptypes/FixupState
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
 - FixupState
---

# FixupState enumeration


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FixupState</b> enumeration  defines the fix-up state of the System Health Agent (SHA).

## -enum-fields

### -field fixupStateSuccess:0

SHA fix-up is successful.

### -field fixupStateInProgress:1

SHA fix-up in progress.

### -field fixupStateCouldNotUpdate:2

SHA could not be updated.

