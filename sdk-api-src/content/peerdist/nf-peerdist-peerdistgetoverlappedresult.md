---
UID: NF:peerdist.PeerDistGetOverlappedResult
title: PeerDistGetOverlappedResult function
author: windows-sdk-content
description: The PeerDistGetOverlappedResult function retrieves the results of asynchronous operations.
old-location: p2p\peerdistgetoverlappedresult.htm
old-project: P2PSdk
ms.assetid: 09feff6e-fa74-4212-8345-09a11cc026c7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerDistGetOverlappedResult, PeerDistGetOverlappedResult function [Peer Networking], p2p.peerdistgetoverlappedresult, peerdist/PeerDistGetOverlappedResult
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	peerdist.h
api_name:
-	PeerDistGetOverlappedResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerDistGetOverlappedResult function


## -description


The <b>PeerDistGetOverlappedResult</b> function retrieves the results of asynchronous operations. This function replaces the <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function for Peer Distribution asynchronous operations.


## -parameters




### -param lpOverlapped [in]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that was specified when the overlapped operation was started.


### -param lpNumberOfBytesTransferred [out]

A pointer to a variable that receives the number of bytes that were actually transferred by a read or write operation. 


### -param bWait [in]

If this parameter is TRUE, the function does not return until the operation has been completed. If this parameter is FALSE and the operation is still pending, the function returns FALSE.

