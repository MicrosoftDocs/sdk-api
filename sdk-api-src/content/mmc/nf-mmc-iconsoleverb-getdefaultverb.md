---
UID: NF:mmc.IConsoleVerb.GetDefaultVerb
title: IConsoleVerb::GetDefaultVerb (mmc.h)
description: The GetDefaultVerb method gets the snap-in's default verb.
helpviewer_keywords: ["GetDefaultVerb","GetDefaultVerb method [MMC]","GetDefaultVerb method [MMC]","IConsoleVerb interface","IConsoleVerb interface [MMC]","GetDefaultVerb method","IConsoleVerb.GetDefaultVerb","IConsoleVerb::GetDefaultVerb","_slate_iconsoleverb_getdefaultverb","mmc.iconsoleverb_getdefaultverb","mmc/IConsoleVerb::GetDefaultVerb"]
old-location: mmc\iconsoleverb_getdefaultverb.htm
tech.root: mmc
ms.assetid: e30f3690-361b-4aee-97e7-014e2e8ee6a4
ms.date: 12/05/2018
ms.keywords: GetDefaultVerb, GetDefaultVerb method [MMC], GetDefaultVerb method [MMC],IConsoleVerb interface, IConsoleVerb interface [MMC],GetDefaultVerb method, IConsoleVerb.GetDefaultVerb, IConsoleVerb::GetDefaultVerb, _slate_iconsoleverb_getdefaultverb, mmc.iconsoleverb_getdefaultverb, mmc/IConsoleVerb::GetDefaultVerb
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
 - IConsoleVerb::GetDefaultVerb
 - mmc/IConsoleVerb::GetDefaultVerb
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
 - IConsoleVerb.GetDefaultVerb
---

# IConsoleVerb::GetDefaultVerb


## -description

The 
GetDefaultVerb method gets the snap-in's default verb.

## -parameters

### -param peCmdID [out]

A pointer to where the snap-in's default verb is returned.

## -returns

This method can return one of these values.

## -remarks

The 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_console_verb">MMC_CONSOLE_VERB</a> enumeration defines the set of default verbs.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setdefaultverb">IConsoleVerb::SetDefaultVerb</a>



<a href="/windows/desktop/api/mmc/ne-mmc-mmc_console_verb">MMC_CONSOLE_VERB</a>