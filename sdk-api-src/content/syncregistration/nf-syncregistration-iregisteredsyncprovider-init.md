---
UID: NF:syncregistration.IRegisteredSyncProvider.Init
title: IRegisteredSyncProvider::Init
author: windows-sdk-content
description: Initializes the synchronization provider before it is ready for a synchronization session.
old-location: winsync\iregisteredsyncprovider_init.htm
old-project: winsync
ms.assetid: 1f022a6b-8f8c-4def-9ca9-dc06ec80f020
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IRegisteredSyncProvider interface [Windows Sync],Init method, IRegisteredSyncProvider.Init, IRegisteredSyncProvider::Init, Init, Init method [Windows Sync], Init method [Windows Sync],IRegisteredSyncProvider interface, syncregistration/IRegisteredSyncProvider::Init, winsync.iregisteredsyncprovider_init
ms.prod: windows
ms.technology: windows-sdk
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
 - IRegisteredSyncProvider.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisteredSyncProvider::Init


## -description


Initializes the synchronization provider before it is ready for a synchronization session.


## -parameters




### -param pguidInstanceId [in]

The instance ID of the synchronization provider.


### -param pguidContentType [in]

A GUID that represents the content type that this provider will synchronize.


### -param pContextPropertyStore [in]

The properties needed to initialize the synchronization provider. These properties are also provided when the synchronization provider is registered.


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




<a href="https://msdn.microsoft.com/53970f17-2857-4624-8594-069cceb93b1e">IRegisteredSyncProvider Interface</a>
 

 

