---
UID: NF:peerdist.PeerDistGetOverlappedResult
title: PeerDistGetOverlappedResult function (peerdist.h)
description: The PeerDistGetOverlappedResult function retrieves the results of asynchronous operations.
helpviewer_keywords: ["PeerDistGetOverlappedResult","PeerDistGetOverlappedResult function [Peer Networking]","p2p.peerdistgetoverlappedresult","peerdist/PeerDistGetOverlappedResult"]
old-location: p2p\peerdistgetoverlappedresult.htm
tech.root: p2p
ms.assetid: 09feff6e-fa74-4212-8345-09a11cc026c7
ms.date: 12/05/2018
ms.keywords: PeerDistGetOverlappedResult, PeerDistGetOverlappedResult function [Peer Networking], p2p.peerdistgetoverlappedresult, peerdist/PeerDistGetOverlappedResult
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
 - PeerDistGetOverlappedResult
 - peerdist/PeerDistGetOverlappedResult
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
 - PeerDistGetOverlappedResult
---

## -description

The <b>PeerDistGetOverlappedResult</b> function retrieves the results of asynchronous operations. This function replaces the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function for Peer Distribution asynchronous operations.

## -parameters

### -param lpOverlapped [in]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that was specified when the overlapped operation was started.

### -param lpNumberOfBytesTransferred [out]

A pointer to a variable that receives the number of bytes that were actually transferred by a read or write operation.

### -param bWait [in]

If this parameter is `true`, the function does not return until the operation has been completed. If this parameter is `false` and the operation is still pending, the function returns `false`.

## -returns

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if the operation has completed. `false` if the *bWait* argument is `false` and the operation is still pending.