---
UID: NF:syncregistration.IRegisteredSyncProvider.Reset
title: IRegisteredSyncProvider::Reset (syncregistration.h)
author: windows-sdk-content
description: Resets a synchronization provider so that it looks like a new replica in the next synchronization session.
old-location: winsync\iregisteredsyncprovider_reset.htm
tech.root: winsync
ms.assetid: 05fe5db8-9a21-4e09-a1fb-d50d1f08a540
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRegisteredSyncProvider interface [Windows Sync],Reset method, IRegisteredSyncProvider.Reset, IRegisteredSyncProvider::Reset, Reset, Reset method [Windows Sync], Reset method [Windows Sync],IRegisteredSyncProvider interface, syncregistration/IRegisteredSyncProvider::Reset, winsync.iregisteredsyncprovider_reset
ms.topic: method
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
 - IRegisteredSyncProvider.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegisteredSyncProvider::Reset


## -description


Resets a synchronization provider so that it looks like a new replica
	in the next synchronization session.


## -parameters






## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The writer of a synchronization provider may choose not to implement this method.




## -see-also




<a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider Interface</a>
 

 

