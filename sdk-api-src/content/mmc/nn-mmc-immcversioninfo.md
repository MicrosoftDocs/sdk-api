---
UID: NN:mmc.IMMCVersionInfo
title: IMMCVersionInfo (mmc.h)
author: windows-sdk-content
description: The IMMCVersionInfo interface provides version information about the installed MMC application.
old-location: mmc\immcversioninfo.htm
tech.root: mmc
ms.assetid: 13cc0cef-3548-4f9f-b150-4f13be23d0ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMMCVersionInfo, IMMCVersionInfo interface [MMC], IMMCVersionInfo interface [MMC],described, MMCVersionInfo, _slate_immcversioninfo, mmc.immcversioninfo, mmc/IMMCVersionInfo
ms.topic: interface
f1_keywords: 
 - "mmc/IMMCVersionInfo"
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
req.lib: Mmc.lib
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
 - IMMCVersionInfo
 - MMCVersionInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMMCVersionInfo interface


## -description


The 
<b>IMMCVersionInfo</b> interface provides version information about the installed MMC application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMCVersionInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMCVersionInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMMCVersionInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-immcversioninfo-getmmcversion">GetMMCVersion</a>
</td>
<td align="left" width="63%">
Returns version information about the installed MMC application.

</td>
</tr>
</table> 

