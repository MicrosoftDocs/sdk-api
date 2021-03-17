---
UID: NF:peerdist.PeerDistServerOpenContentInformation
title: PeerDistServerOpenContentInformation function (peerdist.h)
description: PeerDistServerOpenContentInformation function opens a PEERDIST_CONTENTINFO_HANDLE. The client uses the handle to retrieve content information.
helpviewer_keywords: ["PeerDistServerOpenContentInformation","PeerDistServerOpenContentInformation function [Peer Networking]","p2p.peerdistserveropencontentinformation","peerdist/PeerDistServerOpenContentInformation"]
old-location: p2p\peerdistserveropencontentinformation.htm
tech.root: p2p
ms.assetid: 17b07141-2786-4192-ba7b-f3210c10aad4
ms.date: 12/05/2018
ms.keywords: PeerDistServerOpenContentInformation, PeerDistServerOpenContentInformation function [Peer Networking], p2p.peerdistserveropencontentinformation, peerdist/PeerDistServerOpenContentInformation
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistServerOpenContentInformation
 - peerdist/PeerDistServerOpenContentInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistServerOpenContentInformation
---

# PeerDistServerOpenContentInformation function


## -description

The <b>PeerDistServerOpenContentInformation</b> function opens a <b>PEERDIST_CONTENTINFO_HANDLE</b>. The client uses the handle to retrieve content information.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param cbContentIdentifier

The length, in bytes, of the content identifier.

### -param pContentIdentifier [in]

Pointer to a buffer that contains the content identifier.

### -param ullContentOffset

An offset from the beginning of the published content for which the content information handle is requested.

### -param cbContentLength

The length, in bytes, of the content (starting from the ullContentOffset) for which the content information is requested.

### -param hCompletionPort [in, optional]

A handle to the completion port used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

### -param phContentInfo [out]

A handle  used to retrieve the content information.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
 One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPeerDist</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified content identifier data  is not published.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The feature is disabled by Group Policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The service is unavailable.

</td>
</tr>
</table>

## -remarks

If function succeeds, the handle received by <i>phContentInfo</i> can be passed to the  
 <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a> function to retrieve content information.
The  handle   must be closed via the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosecontentinformation">PeerDistServerCloseContentInformation</a> function.


If <i>ullContentOffset</i> and <i>cbContentLength</i> are both zero, then the content information for the whole content will be retrieved.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a>