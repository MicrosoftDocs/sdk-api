---
UID: NN:mmc.IConsoleVerb
title: IConsoleVerb (mmc.h)
description: The IConsoleVerb interface allows snap-ins to enable standard verbs including cut, copy, paste, delete, properties, rename, refresh, and print. When an item is selected, the snap-in can update the state of these verbs.helpviewer_keywords: ["IConsoleVerb","IConsoleVerb interface [MMC]","IConsoleVerb interface [MMC]","described","_slate_iconsoleverb","mmc.iconsoleverb","mmc/IConsoleVerb"]
old-location: mmc\iconsoleverb.htm
tech.root: mmc
ms.assetid: 9c4338c1-eb5e-47f3-8b5b-0623690bd5f6
ms.date: 12/05/2018
ms.keywords: IConsoleVerb, IConsoleVerb interface [MMC], IConsoleVerb interface [MMC],described, _slate_iconsoleverb, mmc.iconsoleverb, mmc/IConsoleVerb
f1_keywords:
- mmc/IConsoleVerb
dev_langs:
- c++
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
- IConsoleVerb
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConsoleVerb interface


## -description


The 
<b>IConsoleVerb</b> interface allows snap-ins to enable standard verbs including cut, copy, paste, delete, properties, rename, refresh, and print. When an item is selected, the snap-in can update the state of these verbs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsoleVerb</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConsoleVerb</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsoleVerb</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsoleverb-getdefaultverb">GetDefaultVerb</a>
</td>
<td align="left" width="63%">
Gets the default verb.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsoleverb-getverbstate">GetVerbState</a>
</td>
<td align="left" width="63%">
Gets the state of a verb.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setdefaultverb">SetDefaultVerb</a>
</td>
<td align="left" width="63%">
Sets the default verb.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsoleverb-setverbstate">SetVerbState</a>
</td>
<td align="left" width="63%">
Sets the state of a verb.

</td>
</tr>
</table> 


## -remarks



IID_IConsoleVerb is defined as E49F7A60-74AF-11D0-A286-00C04FD8FE93.



