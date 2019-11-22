---
UID: NN:syncregistration.IRegisteredSyncProvider
title: IRegisteredSyncProvider (syncregistration.h)

description: Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider.
old-location: winsync\iregisteredsyncprovider.htm
tech.root: winsync
ms.assetid: 53970f17-2857-4624-8594-069cceb93b1e

ms.date: 12/05/2018
ms.keywords: IRegisteredSyncProvider, IRegisteredSyncProvider interface [Windows Sync], IRegisteredSyncProvider interface [Windows Sync],described, syncregistration/IRegisteredSyncProvider, winsync.iregisteredsyncprovider
ms.topic: interface
f1_keywords: 
 - "syncregistration/IRegisteredSyncProvider"
dev_langs:
 - c++
req.header: syncregistration.h
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
 - Syncregistration.h
api_name:
 - IRegisteredSyncProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegisteredSyncProvider interface


## -description


Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisteredSyncProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRegisteredSyncProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRegisteredSyncProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-iregisteredsyncprovider-getinstanceid">GetInstanceId</a>
</td>
<td align="left" width="63%">
Returns the synchronization provider's instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-iregisteredsyncprovider-init">Init</a>
</td>
<td align="left" width="63%">
Initializes the synchronization provider before it is ready for a synchronization session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-iregisteredsyncprovider-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets a synchronization provider so that it looks like a new replica
	in the next synchronization session.

</td>
</tr>
</table> 


## -remarks



If the registered synchronization provider is a <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a> provider, then the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-iregisteredsyncprovider-init">Init</a>method will be called by the Sync Framework synchronization session. For more information about the different types of synchronization providers you can write for Windows, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

