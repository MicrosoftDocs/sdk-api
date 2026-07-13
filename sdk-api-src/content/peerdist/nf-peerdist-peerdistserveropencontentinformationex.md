---
UID: NF:peerdist.PeerDistServerOpenContentInformationEx
title: PeerDistServerOpenContentInformationEx function (peerdist.h)
description: PeerDistServerOpenContentInformationEx function opens a PEERDIST_CONTENTINFO_HANDLE. The client uses the handle to retrieve content information.
helpviewer_keywords: ["PeerDistServerOpenContentInformationEx","PeerDistServerOpenContentInformationEx function [Peer Networking]","p2p.peerdistserveropencontentinformationex","peerdist/PeerDistServerOpenContentInformationEx"]
old-location: p2p\peerdistserveropencontentinformationex.htm
tech.root: p2p
ms.assetid: cba9a9e8-2397-4c78-925f-ee5d817d1ee4
ms.date: 12/05/2018
ms.keywords: PeerDistServerOpenContentInformationEx, PeerDistServerOpenContentInformationEx function [Peer Networking], p2p.peerdistserveropencontentinformationex, peerdist/PeerDistServerOpenContentInformationEx
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistServerOpenContentInformationEx
 - peerdist/PeerDistServerOpenContentInformationEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PeerDistServerOpenContentInformationEx
---

# PeerDistServerOpenContentInformationEx function


## -description

The <b>PeerDistServerOpenContentInformationEx</b> function opens a <b>PEERDIST_CONTENTINFO_HANDLE</b>. The client uses the handle to retrieve content information.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param cbContentIdentifier [in]

The length, in bytes, of the content identifier.

### -param pContentIdentifier [in]

Pointer to a buffer that contains the content identifier.

### -param ullContentOffset

An offset from the beginning of the published content for which the content information handle is requested.

### -param cbContentLength

The length, in bytes, of the content (starting from the ullContentOffset) for which the content information is requested.

### -param pRetrievalOptions [in]

A <a href="/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options">PEER_RETRIEVAL_OPTIONS</a> structure specifying additional options for retrieving content information.

### -param hCompletionPort [in, optional]

A handle to the completion port used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

### -param phContentInfo [out]

A handle  used to retrieve the content information.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

If function succeeds, the handle received by <i>phContentInfo</i> can be passed to the  
 <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a> function to retrieve content information.
The  handle   must be closed via the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosecontentinformation">PeerDistServerCloseContentInformation</a> function.


If <i>ullContentOffset</i> and <i>cbContentLength</i> are both zero, then the content information for the whole content will be retrieved.

The <i>pRetrievalOptions</i> parameter can be used to specify the range of content information versions that the requesting client is configured to process. This enables the client to retrieve an applicable version of the content information structure.

## -see-also

<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>



<a href="/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options">PEER_RETRIEVAL_OPTIONS</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosecontentinformation">PeerDistServerCloseContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>