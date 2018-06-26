---
UID: NF:mmc.IConsoleVerb.GetDefaultVerb
title: IConsoleVerb::GetDefaultVerb
author: windows-sdk-content
description: The GetDefaultVerb method gets the snap-in's default verb.
old-location: mmc\iconsoleverb_getdefaultverb.htm
old-project: MMC
ms.assetid: e30f3690-361b-4aee-97e7-014e2e8ee6a4
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetDefaultVerb, GetDefaultVerb method [MMC], GetDefaultVerb method [MMC],IConsoleVerb interface, IConsoleVerb interface [MMC],GetDefaultVerb method, IConsoleVerb.GetDefaultVerb, IConsoleVerb::GetDefaultVerb, _slate_iconsoleverb_getdefaultverb, mmc.iconsoleverb_getdefaultverb, mmc/IConsoleVerb::GetDefaultVerb
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
 - IConsoleVerb.GetDefaultVerb
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsoleVerb::GetDefaultVerb


## -description


The 
GetDefaultVerb method gets the snap-in's default verb.


## -parameters




### -param peCmdID






#### - peCmID [out]

A pointer to where the snap-in's default verb is returned.


## -returns



This method can return one of these values.




## -remarks



The 
<a href="https://msdn.microsoft.com/153d89f4-03de-429a-9f52-36a5f6a9762f">MMC_CONSOLE_VERB</a> enumeration defines the set of default verbs.




## -see-also




<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a>



<a href="https://msdn.microsoft.com/099a5cd7-b1c8-45c0-a109-7e78d1b6ee98">IConsoleVerb::SetDefaultVerb</a>



<a href="https://msdn.microsoft.com/153d89f4-03de-429a-9f52-36a5f6a9762f">MMC_CONSOLE_VERB</a>
 

 

