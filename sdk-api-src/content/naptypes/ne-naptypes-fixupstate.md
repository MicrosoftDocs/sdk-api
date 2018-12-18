---
UID: NE:naptypes.tagFixupState
title: FixupState
author: windows-sdk-content
description: Defines the fix-up state of the System Health Agent (SHA).
old-location: nap\fixupstate_enum.htm
tech.root: NAP
ms.assetid: cde1f9df-f4d9-4601-a513-e00639ee9b6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FixupState, FixupState enumeration [NAP], fixupStateCouldNotUpdate, fixupStateInProgress, fixupStateSuccess, nap.fixupstate_enum, naptypes/FixupState, naptypes/fixupStateCouldNotUpdate, naptypes/fixupStateInProgress, naptypes/fixupStateSuccess
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - FixupState
product: Windows
targetos: Windows
req.typenames: FixupState
req.redist: 
---

# FixupState enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FixupState</b> enumeration  defines the fix-up state of the System Health Agent (SHA).


## -enum-fields




### -field fixupStateSuccess

SHA fix-up is successful.


### -field fixupStateInProgress

SHA fix-up in progress.


### -field fixupStateCouldNotUpdate

SHA could not be updated.

