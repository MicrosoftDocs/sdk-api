---
UID: NF:mmc.IConsoleVerb.SetVerbState
title: IConsoleVerb::SetVerbState (mmc.h)
description: The SetVerbState method enables a snap-in to set a given verb's button state.
helpviewer_keywords: ["IConsoleVerb interface [MMC]","SetVerbState method","IConsoleVerb.SetVerbState","IConsoleVerb::SetVerbState","SetVerbState","SetVerbState method [MMC]","SetVerbState method [MMC]","IConsoleVerb interface","_slate_iconsoleverb_setverbstate","mmc.iconsoleverb_setverbstate","mmc/IConsoleVerb::SetVerbState"]
old-location: mmc\iconsoleverb_setverbstate.htm
tech.root: mmc
ms.assetid: 55cf5f73-a113-430e-be16-d7a88abe15b6
ms.date: 12/05/2018
ms.keywords: IConsoleVerb interface [MMC],SetVerbState method, IConsoleVerb.SetVerbState, IConsoleVerb::SetVerbState, SetVerbState, SetVerbState method [MMC], SetVerbState method [MMC],IConsoleVerb interface, _slate_iconsoleverb_setverbstate, mmc.iconsoleverb_setverbstate, mmc/IConsoleVerb::SetVerbState
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
 - IConsoleVerb::SetVerbState
 - mmc/IConsoleVerb::SetVerbState
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
 - IConsoleVerb.SetVerbState
---

# IConsoleVerb::SetVerbState


## -description

The 
SetVerbState method enables a snap-in to set a given verb's button state.

## -parameters

### -param eCmdID [in]

A value that specifies the command identifier of the verb. Values are taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_console_verb">MMC_CONSOLE_VERB</a> enumeration. This value cannot be MMC_VERB_NONE.

### -param nState [in]

Identifies the possible states of the button. Taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_button_state">MMC_BUTTON_STATE</a> enumeration.

### -param bState [in]

This value is <b>TRUE</b> to enable or hide the verb, <b>FALSE</b> to disable or show the selected verb.

## -returns

This method can return one of these values.

## -remarks

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a>