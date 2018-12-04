---
UID: NF:winsync.ISyncSessionState2.SetProviderWithError
title: ISyncSessionState2::SetProviderWithError
author: windows-sdk-content
description: Indicates which provider caused synchronization to fail.
old-location: winsync\isyncsessionstate2_setproviderwitherror.htm
tech.root: winsync
ms.assetid: dcbfcc13-5a8f-4062-baef-899f81413768
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISyncSessionState2 interface [Windows Sync],SetProviderWithError method, ISyncSessionState2.SetProviderWithError, ISyncSessionState2::SetProviderWithError, SetProviderWithError, SetProviderWithError method [Windows Sync], SetProviderWithError method [Windows Sync],ISyncSessionState2 interface, winsync.isyncsessionstate2_setproviderwitherror, winsync/ISyncSessionState2::SetProviderWithError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - Winsync.h
api_name:
 - ISyncSessionState2.SetProviderWithError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncSessionState2::SetProviderWithError


## -description


Indicates which provider caused synchronization to fail.


## -parameters




### -param fSelf [in]

<b>TRUE</b> when the provider that calls this method is the provider that caused the error. Otherwise,<b> FALSE</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A synchronization session does not exist.

</td>
</tr>
</table>
 




## -remarks



The destination provider indicates which provider caused synchronization to fail during processing of the <a href="https://msdn.microsoft.com/528a109a-9c11-4e20-b3d5-9bb7241d02b6">IKnowledgeSyncProvider::ProcessChangeBatch</a> method, by using <b>ISyncSessionState2::SetProviderWithError</b>. <b>ISyncSessionState2::SetProviderWithError</b> is used by an application to obtain the <a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider</a> interface of the provider that caused the failure. The synchronization session can then query for other interfaces that are implemented by the provider, and call methods to handle the error.





## -see-also




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>



<a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider Interface</a>



<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>



<a href="https://msdn.microsoft.com/c98e675f-48f4-4ffa-bc81-18a58edd8c34">ISyncSessionState2 Interface</a>
 

 

