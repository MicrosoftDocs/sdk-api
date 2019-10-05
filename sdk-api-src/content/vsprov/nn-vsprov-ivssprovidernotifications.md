---
UID: NN:vsprov.IVssProviderNotifications
title: IVssProviderNotifications (vsprov.h)
author: windows-sdk-content
description: The IVssProviderNotifications interface manages providers registered with VSS.
old-location: base\ivssprovidernotifications.htm
tech.root: VSS
ms.assetid: 09324f54-8902-43d1-a4f9-967adccbf8be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssProviderNotifications, IVssProviderNotifications interface [VSS], IVssProviderNotifications interface [VSS],described, base.ivssprovidernotifications, vsprov/IVssProviderNotifications
ms.topic: interface
f1_keywords: 
 - "vsprov/IVssProviderNotifications"
dev_langs:
 - c++
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssProviderNotifications
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssProviderNotifications interface


## -description


The <b>IVssProviderNotifications</b> interface 
   manages providers registered with VSS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssProviderNotifications</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssProviderNotifications</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssProviderNotifications</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidernotifications-onload">OnLoad</a>
</td>
<td align="left" width="63%">
Notifies the provider that it was just loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidernotifications-onunload">OnUnload</a>
</td>
<td align="left" width="63%">
Notifies the provider that it was just unloaded.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
 

 

