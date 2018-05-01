---
UID: NF:peerdist.PeerDistServerOpenContentInformationEx
title: PeerDistServerOpenContentInformationEx function
author: windows-driver-content
description: PeerDistServerOpenContentInformationEx function opens a PEERDIST_CONTENTINFO_HANDLE. The client uses the handle to retrieve content information.
old-location: p2p\peerdistserveropencontentinformationex.htm
old-project: P2PSdk
ms.assetid: cba9a9e8-2397-4c78-925f-ee5d817d1ee4
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PeerDistServerOpenContentInformationEx, PeerDistServerOpenContentInformationEx function [Peer Networking], p2p.peerdistserveropencontentinformationex, peerdist/PeerDistServerOpenContentInformationEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	peerdist.h
api_name:
-	PeerDistServerOpenContentInformationEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerDistServerOpenContentInformationEx function


## -description


The <b>PeerDistServerOpenContentInformationEx</b> function opens a <b>PEERDIST_CONTENTINFO_HANDLE</b>. The client uses the handle to retrieve content information.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param cbContentIdentifier [in]

The length, in bytes, of the content identifier.


### -param pContentIdentifier [in]

Pointer to a buffer that contains the content identifier.


### -param ullContentOffset

An offset from the beginning of the published content for which the content information handle is requested.


### -param cbContentLength

The length, in bytes, of the content (starting from the ullContentOffset) for which the content information is requested.


### -param pRetrievalOptions [in]

A <a href="https://msdn.microsoft.com/cc5953bd-39cc-472e-a84b-89be7a6e6d09">PEER_RETRIEVAL_OPTIONS</a> structure specifying additional options for retrieving content information.


### -param hCompletionPort [in, optional]

A handle to the completion port used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param phContentInfo [out]

A handle  used to retrieve the content information.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



If function succeeds, the handle received by <i>phContentInfo</i> can be passed to the  
 <a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a> function to retrieve content information.
The  handle   must be closed via the <a href="https://msdn.microsoft.com/066f1856-0617-40c7-a444-9765c01b4563">PeerDistServerCloseContentInformation</a> function.


If <i>ullContentOffset</i> and <i>cbContentLength</i> are both zero, then the content information for the whole content will be retrieved.

The <i>pRetrievalOptions</i> parameter can be used to specify the range of content information versions that the requesting client is configured to process. This enables the client to retrieve an applicable version of the content information structure.




## -see-also




<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>



<a href="https://msdn.microsoft.com/cc5953bd-39cc-472e-a84b-89be7a6e6d09">PEER_RETRIEVAL_OPTIONS</a>



<a href="https://msdn.microsoft.com/066f1856-0617-40c7-a444-9765c01b4563">PeerDistServerCloseContentInformation</a>



<a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

