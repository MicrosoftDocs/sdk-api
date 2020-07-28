---
UID: NN:winsync.ISyncProvider
title: ISyncProvider (winsync.h)
description: Represents a synchronization provider that can be used by a synchronization session to synchronize data with another synchronization provider.
helpviewer_keywords: ["ISyncProvider","ISyncProvider interface [Windows Sync]","ISyncProvider interface [Windows Sync]","described","winsync.isyncprovider","winsync/ISyncProvider"]
old-location: winsync\isyncprovider.htm
tech.root: winsync
ms.assetid: 0664267f-90ba-4123-bfe5-7cf748b78c10
ms.date: 12/05/2018
ms.keywords: ISyncProvider, ISyncProvider interface [Windows Sync], ISyncProvider interface [Windows Sync],described, winsync.isyncprovider, winsync/ISyncProvider
f1_keywords:
- winsync/ISyncProvider
dev_langs:
- c++
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- winsync.h
api_name:
- ISyncProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncProvider interface


## -description


Represents a synchronization provider that can be used by a synchronization session to synchronize data with another synchronization provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncprovider-getidparameters">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

