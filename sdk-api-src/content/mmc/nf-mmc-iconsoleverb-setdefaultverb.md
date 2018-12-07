---
UID: NF:mmc.IConsoleVerb.SetDefaultVerb
title: IConsoleVerb::SetDefaultVerb
author: windows-sdk-content
description: The SetDefaultVerb method sets the default action on an object.
old-location: mmc\iconsoleverb_setdefaultverb.htm
tech.root: mmc
ms.assetid: 099a5cd7-b1c8-45c0-a109-7e78d1b6ee98
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IConsoleVerb interface [MMC],SetDefaultVerb method, IConsoleVerb.SetDefaultVerb, IConsoleVerb::SetDefaultVerb, SetDefaultVerb, SetDefaultVerb method [MMC], SetDefaultVerb method [MMC],IConsoleVerb interface, _slate_iconsoleverb_setdefaultverb, mmc.iconsoleverb_setdefaultverb, mmc/IConsoleVerb::SetDefaultVerb
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
 - IConsoleVerb.SetDefaultVerb
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsoleVerb::SetDefaultVerb


## -description


The 
<b>SetDefaultVerb</b> method sets the default action on an object.


## -parameters




### -param eCmdID [in]

The default verb.


## -returns



This method can return one of these values.




## -remarks



The 
<a href="https://msdn.microsoft.com/153d89f4-03de-429a-9f52-36a5f6a9762f">MMC_CONSOLE_VERB</a> enumeration defines the set of default verbs. The snap-in can set any verb as the default verb. Setting a default verb causes MMC to:

<ul>
<li>Show the context menu item for the verb in bold.</li>
<li>Perform a default action (only for properties and open verbs) if the snap-in returns S_FALSE in its <a href="https://msdn.microsoft.com/0c85cd06-4799-4bb6-aa1d-3386edbf1a37">MMCN_DBLCLICK</a> notification handler.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a>



<a href="https://msdn.microsoft.com/e30f3690-361b-4aee-97e7-014e2e8ee6a4">IConsoleVerb::GetDefaultVerb</a>



<a href="https://msdn.microsoft.com/153d89f4-03de-429a-9f52-36a5f6a9762f">MMC_CONSOLE_VERB</a>
 

 

