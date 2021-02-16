---
UID: NF:mmc.IConsoleVerb.SetDefaultVerb
title: IConsoleVerb::SetDefaultVerb (mmc.h)
description: The SetDefaultVerb method sets the default action on an object.
helpviewer_keywords: ["IConsoleVerb interface [MMC]","SetDefaultVerb method","IConsoleVerb.SetDefaultVerb","IConsoleVerb::SetDefaultVerb","SetDefaultVerb","SetDefaultVerb method [MMC]","SetDefaultVerb method [MMC]","IConsoleVerb interface","_slate_iconsoleverb_setdefaultverb","mmc.iconsoleverb_setdefaultverb","mmc/IConsoleVerb::SetDefaultVerb"]
old-location: mmc\iconsoleverb_setdefaultverb.htm
tech.root: mmc
ms.assetid: 099a5cd7-b1c8-45c0-a109-7e78d1b6ee98
ms.date: 12/05/2018
ms.keywords: IConsoleVerb interface [MMC],SetDefaultVerb method, IConsoleVerb.SetDefaultVerb, IConsoleVerb::SetDefaultVerb, SetDefaultVerb, SetDefaultVerb method [MMC], SetDefaultVerb method [MMC],IConsoleVerb interface, _slate_iconsoleverb_setdefaultverb, mmc.iconsoleverb_setdefaultverb, mmc/IConsoleVerb::SetDefaultVerb
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
 - IConsoleVerb::SetDefaultVerb
 - mmc/IConsoleVerb::SetDefaultVerb
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
 - IConsoleVerb.SetDefaultVerb
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
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_console_verb">MMC_CONSOLE_VERB</a> enumeration defines the set of default verbs. The snap-in can set any verb as the default verb. Setting a default verb causes MMC to:

<ul>
<li>Show the context menu item for the verb in bold.</li>
<li>Perform a default action (only for properties and open verbs) if the snap-in returns S_FALSE in its <a href="/previous-versions/windows/desktop/mmc/mmcn-dblclick">MMCN_DBLCLICK</a> notification handler.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iconsoleverb-getdefaultverb">IConsoleVerb::GetDefaultVerb</a>



<a href="/windows/desktop/api/mmc/ne-mmc-mmc_console_verb">MMC_CONSOLE_VERB</a>