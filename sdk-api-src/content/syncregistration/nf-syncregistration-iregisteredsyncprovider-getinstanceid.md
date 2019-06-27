---
UID: NF:syncregistration.IRegisteredSyncProvider.GetInstanceId
title: IRegisteredSyncProvider::GetInstanceId (syncregistration.h)
author: windows-sdk-content
description: Returns the synchronization provider's instance ID.
old-location: winsync\iregisteredsyncprovider_getinstanceid.htm
tech.root: winsync
ms.assetid: d8206138-92cc-4ed7-937e-baf2ed432b6b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInstanceId, GetInstanceId method [Windows Sync], GetInstanceId method [Windows Sync],IRegisteredSyncProvider interface, IRegisteredSyncProvider interface [Windows Sync],GetInstanceId method, IRegisteredSyncProvider.GetInstanceId, IRegisteredSyncProvider::GetInstanceId, syncregistration/IRegisteredSyncProvider::GetInstanceId, winsync.iregisteredsyncprovider_getinstanceid
ms.topic: method
f1_keywords: 
 - "syncregistration/IRegisteredSyncProvider.GetInstanceId"
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
 - IRegisteredSyncProvider.GetInstanceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegisteredSyncProvider::GetInstanceId


## -description


Returns the synchronization provider's instance ID.


## -parameters




### -param pguidInstanceId [out]

The instance ID of the synchronization provider.


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
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-iregisteredsyncprovider">IRegisteredSyncProvider Interface</a>
 

 

