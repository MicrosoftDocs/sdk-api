---
UID: NF:bits4_0.IBackgroundCopyFile4.GetPeerDownloadStats
title: IBackgroundCopyFile4::GetPeerDownloadStats
author: windows-sdk-content
description: Specifies statistics about the amount of data downloaded from peers and origin servers.
old-location: bits\ibackgroundcopyfile4_getpeerdownloadstats.htm
tech.root: Bits
ms.assetid: dff90887-90d5-48a4-a400-31d99de27d39
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPeerDownloadStats, GetPeerDownloadStats method [BITS], GetPeerDownloadStats method [BITS],IBackgroundCopyFile4 interface, IBackgroundCopyFile4 interface [BITS],GetPeerDownloadStats method, IBackgroundCopyFile4.GetPeerDownloadStats, IBackgroundCopyFile4::GetPeerDownloadStats, bits.ibackgroundcopyfile4_getpeerdownloadstats, bits4_0/IBackgroundCopyFile4::GetPeerDownloadStats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits4_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits4_0.idl
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
 - Bits4_0.h
api_name:
 - IBackgroundCopyFile4.GetPeerDownloadStats
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
- apiref
: 
- COM
: 
- bits4_0.h
: 
- IBackgroundCopyFile4.GetPeerDownloadStats
: 
---

# IBackgroundCopyFile4::GetPeerDownloadStats


## -description


Specifies statistics about the amount of data downloaded from peers and origin servers.


## -parameters




### -param pFromOrigin [out]

Specifies the amount of file data downloaded from the originating server.


### -param pFromPeers [out]

Specifies the amount of file data downloaded from a peer-to-peer source.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd904468(v=VS.85).aspx">IBackgroundCopyFile4</a>
 

 

