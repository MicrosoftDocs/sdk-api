---
UID: NF:mmc.IConsoleVerb.SetVerbState
title: IConsoleVerb::SetVerbState
author: windows-sdk-content
description: The SetVerbState method enables a snap-in to set a given verb's button state.
old-location: mmc\iconsoleverb_setverbstate.htm
tech.root: mmc
ms.assetid: 55cf5f73-a113-430e-be16-d7a88abe15b6
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IConsoleVerb interface [MMC],SetVerbState method, IConsoleVerb.SetVerbState, IConsoleVerb::SetVerbState, SetVerbState, SetVerbState method [MMC], SetVerbState method [MMC],IConsoleVerb interface, _slate_iconsoleverb_setverbstate, mmc.iconsoleverb_setverbstate, mmc/IConsoleVerb::SetVerbState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleVerb.SetVerbState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleVerb::SetVerbState


## -description


The 
SetVerbState method enables a snap-in to set a given verb's button state.


## -parameters




### -param eCmdID [in]

A value that specifies the command identifier of the verb. Values are taken from the 
<a href="https://msdn.microsoft.com/153d89f4-03de-429a-9f52-36a5f6a9762f">MMC_CONSOLE_VERB</a> enumeration. This value cannot be MMC_VERB_NONE.


### -param nState [in]

Identifies the possible states of the button. Taken from the 
<a href="https://msdn.microsoft.com/b08c8905-1a6d-485f-9136-d63efd0e8194">MMC_BUTTON_STATE</a> enumeration.


### -param bState [in]

This value is <b>TRUE</b> to enable or hide the verb, <b>FALSE</b> to disable or show the selected verb.


## -returns



This method can return one of these values.




## -remarks








## -see-also




<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a>
 

 

