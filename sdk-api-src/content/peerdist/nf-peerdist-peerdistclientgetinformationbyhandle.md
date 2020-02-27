---
UID: NF:peerdist.PeerDistClientGetInformationByHandle
title: PeerDistClientGetInformationByHandle function (peerdist.h)
description: The PeerDistClientGetInformationByHandle function retrieves additional information from the Peer Distribution service for a specific content handle.
old-location: p2p\peerdistclientgetinformationbyhandle.htm
tech.root: P2PSdk
ms.assetid: d3bb080c-cde7-4623-95fd-3cffb3bd93aa
ms.date: 12/05/2018
ms.keywords: PeerDistClientGetInformationByHandle, PeerDistClientGetInformationByHandle function [Peer Networking], p2p.peerdistclientgetinformationbyhandle, peerdist/PeerDistClientGetInformationByHandle
f1_keywords:
- peerdist/PeerDistClientGetInformationByHandle
dev_langs:
- c++
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
req.dll: PeerDist.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- PeerDist.dll
api_name:
- PeerDistClientGetInformationByHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerDistClientGetInformationByHandle function


## -description


The <b>PeerDistClientGetInformationByHandle</b> function retrieves additional information from the Peer Distribution service for a specific content handle.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by the <a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a> function.


### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> returned by the <a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a> function.


### -param PeerDistClientInfoClass [in]

A value from the <a href="https://docs.microsoft.com/windows/win32/api/peerdist/ne-peerdist-peerdist_client_info_by_handle_class">PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</a> enumeration that indicates the information to retrieve.


### -param dwBufferSize

The size, in bytes, of the buffer for the <i>lpInformation</i> parameter.


### -param lpInformation [out]

A buffer for the returned information. The format of this information depends on the value of the <i>PeerDistClientInfoClass</i> parameter.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/peerdist/ne-peerdist-peerdist_client_info_by_handle_class">PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>
 

 

