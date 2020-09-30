---
UID: NF:mmc.IConsoleVerb.GetVerbState
title: IConsoleVerb::GetVerbState (mmc.h)
description: The GetVerbState method enables a snap-in to obtain a given verb's current state.
helpviewer_keywords: ["GetVerbState","GetVerbState method [MMC]","GetVerbState method [MMC]","IConsoleVerb interface","IConsoleVerb interface [MMC]","GetVerbState method","IConsoleVerb.GetVerbState","IConsoleVerb::GetVerbState","_slate_iconsoleverb_getverbstate","mmc.iconsoleverb_getverbstate","mmc/IConsoleVerb::GetVerbState"]
old-location: mmc\iconsoleverb_getverbstate.htm
tech.root: mmc
ms.assetid: 86388a22-5156-45e9-a601-33b7c5ca15f3
ms.date: 12/05/2018
ms.keywords: GetVerbState, GetVerbState method [MMC], GetVerbState method [MMC],IConsoleVerb interface, IConsoleVerb interface [MMC],GetVerbState method, IConsoleVerb.GetVerbState, IConsoleVerb::GetVerbState, _slate_iconsoleverb_getverbstate, mmc.iconsoleverb_getverbstate, mmc/IConsoleVerb::GetVerbState
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsoleVerb::GetVerbState
 - mmc/IConsoleVerb::GetVerbState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleVerb.GetVerbState
---

# IConsoleVerb::GetVerbState


## -description

The 
GetVerbState method enables a snap-in to obtain a given verb's current state.

## -parameters

### -param eCmdID [in]

A value that specifies the command identifier of the verb. Taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_console_verb">MMC_CONSOLE_VERB</a> enumeration. This value cannot be MMC_VERB_NONE.

### -param nState [in]

A value that identifies the possible states of the button. Taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_button_state">MMC_BUTTON_STATE</a> enumeration.

### -param pState [out]

A pointer to the state information returned. <b>TRUE</b> if the state is enabled or hidden and <b>FALSE</b> if the state is disabled or visible.

## -returns

This method can return one of these values.

## -remarks

When an item is selected, the verb states for all the commands are reset to disabled and hidden. It is up to the snap-in developer to update the verb state when an item is selected.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a>



<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>