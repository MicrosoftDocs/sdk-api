---
UID: NN:mmc.IRequiredExtensions
title: IRequiredExtensions (mmc.h)
description: The IRequiredExtensions interface is introduced in MMC 1.1.
helpviewer_keywords: ["IRequiredExtensions","IRequiredExtensions interface [MMC]","IRequiredExtensions interface [MMC]","described","_slate_irequiredextensions","mmc.irequiredextensions","mmc/IRequiredExtensions"]
old-location: mmc\irequiredextensions.htm
tech.root: mmc
ms.assetid: 55832db9-30d9-4a5f-bfef-a014b1050f22
ms.date: 12/05/2018
ms.keywords: IRequiredExtensions, IRequiredExtensions interface [MMC], IRequiredExtensions interface [MMC],described, _slate_irequiredextensions, mmc.irequiredextensions, mmc/IRequiredExtensions
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRequiredExtensions
 - mmc/IRequiredExtensions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IRequiredExtensions
---

# IRequiredExtensions interface


## -description

The 
<b>IRequiredExtensions</b> interface is introduced in MMC 1.1.

The 
<b>IRequiredExtensions</b> interface enables a snap-in to add some or all of the extension snap-ins registered for your snap-in.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRequiredExtensions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRequiredExtensions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRequiredExtensions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-enableallextensions">EnableAllExtensions</a>
</td>
<td align="left" width="63%">
Enables all extensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getfirstextension">GetFirstExtension</a>
</td>
<td align="left" width="63%">
Gets first required extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mmc/nf-mmc-irequiredextensions-getnextextension">GetNextExtension</a>
</td>
<td align="left" width="63%">
Gets next required extension.

</td>
</tr>
</table>