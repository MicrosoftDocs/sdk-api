---
UID: NF:mmc.IConsoleVerb.GetVerbState
title: IConsoleVerb::GetVerbState
author: windows-sdk-content
description: The GetVerbState method enables a snap-in to obtain a given verb's current state.
old-location: mmc\iconsoleverb_getverbstate.htm
old-project: mmc
ms.assetid: 86388a22-5156-45e9-a601-33b7c5ca15f3
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetVerbState, GetVerbState method [MMC], GetVerbState method [MMC],IConsoleVerb interface, IConsoleVerb interface [MMC],GetVerbState method, IConsoleVerb.GetVerbState, IConsoleVerb::GetVerbState, _slate_iconsoleverb_getverbstate, mmc.iconsoleverb_getverbstate, mmc/IConsoleVerb::GetVerbState
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleVerb.GetVerbState
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsoleVerb::GetVerbState


## -description


The 
GetVerbState method enables a snap-in to obtain a given verb's current state.


## -parameters




### -param eCmdID [in]

A value that specifies the command identifier of the verb. Taken from the 
<a href="https://msdn.microsoft.com/153d89f4-03de-429a-9f52-36a5f6a9762f">MMC_CONSOLE_VERB</a> enumeration. This value cannot be MMC_VERB_NONE.


### -param nState [in]

A value that identifies the possible states of the button. Taken from the 
<a href="https://msdn.microsoft.com/b08c8905-1a6d-485f-9136-d63efd0e8194">MMC_BUTTON_STATE</a> enumeration.


### -param pState [out]

A pointer to the state information returned. <b>TRUE</b> if the state is enabled or hidden and <b>FALSE</b> if the state is disabled or visible.


## -returns



This method can return one of these values.




## -remarks



When an item is selected, the verb states for all the commands are reset to disabled and hidden. It is up to the snap-in developer to update the verb state when an item is selected.




## -see-also




<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a>



<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

