---
UID: NN:syncregistration.IRegisteredSyncProvider
title: IRegisteredSyncProvider
author: windows-sdk-content
description: Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider.
old-location: winsync\iregisteredsyncprovider.htm
old-project: winsync
ms.assetid: 53970f17-2857-4624-8594-069cceb93b1e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IRegisteredSyncProvider, IRegisteredSyncProvider interface [Windows Sync], IRegisteredSyncProvider interface [Windows Sync],described, syncregistration/IRegisteredSyncProvider, winsync.iregisteredsyncprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - IRegisteredSyncProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisteredSyncProvider interface


## -description


Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisteredSyncProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRegisteredSyncProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d8206138-92cc-4ed7-937e-baf2ed432b6b">GetInstanceId</a>
</td>
<td align="left" width="63%">
Returns the synchronization provider's instance ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the synchronization provider before it is ready for a synchronization session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets a synchronization provider so that it looks like a new replica
	in the next synchronization session.

</td>
</tr>
</table> 


## -remarks



If the registered synchronization provider is a <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a> provider, then the <a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>

method will be called by the Sync Framework synchronization session. For more information about the different types of synchronization providers you can write for Windows, see <a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>.




## -see-also




<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

