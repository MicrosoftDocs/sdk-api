---
UID: NN:natupnp.INATNumberOfEntriesCallback
title: INATNumberOfEntriesCallback (natupnp.h)
author: windows-sdk-content
description: The INATNumberOfEntriesCallback interface provides a method that the system calls if the number of port mappings changes.
old-location: ics\inatnumberofentriescallback.htm
tech.root: ics
ms.assetid: c64e5ce3-78f6-4f51-8ae1-c871c4716d26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INATNumberOfEntriesCallback, INATNumberOfEntriesCallback interface [ICS/ICF], INATNumberOfEntriesCallback interface [ICS/ICF],described, _ics_inatnumberofentriescallback, ics.inatnumberofentriescallback, natupnp/INATNumberOfEntriesCallback
ms.topic: interface
f1_keywords: 
 - "natupnp/INATNumberOfEntriesCallback"
dev_langs:
 - c++
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INATNumberOfEntriesCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INATNumberOfEntriesCallback interface


## -description


The 
<b>INATNumberOfEntriesCallback</b> interface provides a method that the system calls if the number of port mappings changes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INATNumberOfEntriesCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INATNumberOfEntriesCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INATNumberOfEntriesCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-inatnumberofentriescallback-newnumberofentries">NewNumberOfEntries</a>
</td>
<td align="left" width="63%">
Notifies the application when the number of port mappings has changed.

</td>
</tr>
</table> 

