---
UID: NF:winsync.ISyncSessionExtendedErrorInfo.GetSyncProviderWithError
title: ISyncSessionExtendedErrorInfo::GetSyncProviderWithError
author: windows-sdk-content
description: Gets the ISyncProvider interface of the provider that caused synchronization to fail.
old-location: winsync\isyncsessionextendederrorinfo_getsyncproviderwitherror.htm
old-project: winsync
ms.assetid: b0115f1a-41e7-4126-9b77-03960227d4fe
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSyncProviderWithError, GetSyncProviderWithError method [Windows Sync], GetSyncProviderWithError method [Windows Sync],ISyncSessionExtendedErrorInfo interface, ISyncSessionExtendedErrorInfo interface [Windows Sync],GetSyncProviderWithError method, ISyncSessionExtendedErrorInfo.GetSyncProviderWithError, ISyncSessionExtendedErrorInfo::GetSyncProviderWithError, winsync.isyncsessionextendederrorinfo_getsyncproviderwitherror, winsync/ISyncSessionExtendedErrorInfo::GetSyncProviderWithError
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncSessionExtendedErrorInfo.GetSyncProviderWithError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncSessionExtendedErrorInfo::GetSyncProviderWithError


## -description


Gets the <a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider</a> interface of the provider that caused synchronization to fail.


## -parameters




### -param ppProviderWithError [out]

The <a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider</a> interface of the provider that caused synchronization to fail.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
A synchronization session was not started.

</td>
</tr>
</table>
 




## -remarks



The destination provider indicates which provider caused synchronization to fail during processing of the <a href="https://msdn.microsoft.com/528a109a-9c11-4e20-b3d5-9bb7241d02b6">IKnowledgeSyncProvider::ProcessChangeBatch</a> method by using <a href="https://msdn.microsoft.com/dcbfcc13-5a8f-4062-baef-899f81413768">ISyncSessionState2::SetProviderWithError</a>. <b>ISyncSessionExtendedErrorInfo::GetSyncProviderWithError</b> is used by an application to obtain the <a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider</a> interface of the provider that caused the failure. The application can then query for other interfaces that are implemented by the provider, and call methods to handle the error.




## -see-also




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>



<a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider Interface</a>



<a href="https://msdn.microsoft.com/0c6f90af-f4ca-4fa9-8050-acc61b4ee8d2">ISyncSessionExtendedErrorInfo Interface</a>



<a href="https://msdn.microsoft.com/c98e675f-48f4-4ffa-bc81-18a58edd8c34">ISyncSessionState2 Interface</a>
 

 

