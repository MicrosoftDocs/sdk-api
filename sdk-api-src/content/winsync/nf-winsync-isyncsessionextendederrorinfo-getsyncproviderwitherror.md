---
UID: NF:winsync.ISyncSessionExtendedErrorInfo.GetSyncProviderWithError
title: ISyncSessionExtendedErrorInfo::GetSyncProviderWithError (winsync.h)
description: Gets the ISyncProvider interface of the provider that caused synchronization to fail.
helpviewer_keywords: ["GetSyncProviderWithError","GetSyncProviderWithError method [Windows Sync]","GetSyncProviderWithError method [Windows Sync]","ISyncSessionExtendedErrorInfo interface","ISyncSessionExtendedErrorInfo interface [Windows Sync]","GetSyncProviderWithError method","ISyncSessionExtendedErrorInfo.GetSyncProviderWithError","ISyncSessionExtendedErrorInfo::GetSyncProviderWithError","winsync.isyncsessionextendederrorinfo_getsyncproviderwitherror","winsync/ISyncSessionExtendedErrorInfo::GetSyncProviderWithError"]
old-location: winsync\isyncsessionextendederrorinfo_getsyncproviderwitherror.htm
tech.root: winsync
ms.assetid: b0115f1a-41e7-4126-9b77-03960227d4fe
ms.date: 12/05/2018
ms.keywords: GetSyncProviderWithError, GetSyncProviderWithError method [Windows Sync], GetSyncProviderWithError method [Windows Sync],ISyncSessionExtendedErrorInfo interface, ISyncSessionExtendedErrorInfo interface [Windows Sync],GetSyncProviderWithError method, ISyncSessionExtendedErrorInfo.GetSyncProviderWithError, ISyncSessionExtendedErrorInfo::GetSyncProviderWithError, winsync.isyncsessionextendederrorinfo_getsyncproviderwitherror, winsync/ISyncSessionExtendedErrorInfo::GetSyncProviderWithError
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
 - ISyncSessionExtendedErrorInfo::GetSyncProviderWithError
 - winsync/ISyncSessionExtendedErrorInfo::GetSyncProviderWithError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncSessionExtendedErrorInfo.GetSyncProviderWithError
---

# ISyncSessionExtendedErrorInfo::GetSyncProviderWithError


## -description

Gets the <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider</a> interface of the provider that caused synchronization to fail.

## -parameters

### -param ppProviderWithError [out]

The <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider</a> interface of the provider that caused synchronization to fail.

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

The destination provider indicates which provider caused synchronization to fail during processing of the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processchangebatch">IKnowledgeSyncProvider::ProcessChangeBatch</a> method by using <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate2-setproviderwitherror">ISyncSessionState2::SetProviderWithError</a>. <b>ISyncSessionExtendedErrorInfo::GetSyncProviderWithError</b> is used by an application to obtain the <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider</a> interface of the provider that caused the failure. The application can then query for other interfaces that are implemented by the provider, and call methods to handle the error.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionextendederrorinfo">ISyncSessionExtendedErrorInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate2">ISyncSessionState2 Interface</a>