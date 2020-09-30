---
UID: NF:winsync.ISyncSessionState2.SetProviderWithError
title: ISyncSessionState2::SetProviderWithError (winsync.h)
description: Indicates which provider caused synchronization to fail.
helpviewer_keywords: ["ISyncSessionState2 interface [Windows Sync]","SetProviderWithError method","ISyncSessionState2.SetProviderWithError","ISyncSessionState2::SetProviderWithError","SetProviderWithError","SetProviderWithError method [Windows Sync]","SetProviderWithError method [Windows Sync]","ISyncSessionState2 interface","winsync.isyncsessionstate2_setproviderwitherror","winsync/ISyncSessionState2::SetProviderWithError"]
old-location: winsync\isyncsessionstate2_setproviderwitherror.htm
tech.root: winsync
ms.assetid: dcbfcc13-5a8f-4062-baef-899f81413768
ms.date: 12/05/2018
ms.keywords: ISyncSessionState2 interface [Windows Sync],SetProviderWithError method, ISyncSessionState2.SetProviderWithError, ISyncSessionState2::SetProviderWithError, SetProviderWithError, SetProviderWithError method [Windows Sync], SetProviderWithError method [Windows Sync],ISyncSessionState2 interface, winsync.isyncsessionstate2_setproviderwitherror, winsync/ISyncSessionState2::SetProviderWithError
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncSessionState2::SetProviderWithError
 - winsync/ISyncSessionState2::SetProviderWithError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsync.h
api_name:
 - ISyncSessionState2.SetProviderWithError
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

The destination provider indicates which provider caused synchronization to fail during processing of the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processchangebatch">IKnowledgeSyncProvider::ProcessChangeBatch</a> method, by using <b>ISyncSessionState2::SetProviderWithError</b>. <b>ISyncSessionState2::SetProviderWithError</b> is used by an application to obtain the <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider</a> interface of the provider that caused the failure. The synchronization session can then query for other interfaces that are implemented by the provider, and call methods to handle the error.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate2">ISyncSessionState2 Interface</a>