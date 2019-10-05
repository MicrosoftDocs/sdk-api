---
UID: NE:drt.drt_status_tag
title: DRT_STATUS (drt.h)
author: windows-sdk-content
description: The DRT_STATUS enumeration defines the status of a local DRT instance.
old-location: p2p\drt_status.htm
tech.root: P2PSdk
ms.assetid: 4bd81191-862c-4537-9c90-4b9fec270a16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRT_ACTIVE, DRT_ALONE, DRT_FAULTED, DRT_NO_NETWORK, DRT_STATUS, DRT_STATUS enumeration [Peer Networking], drt/DRT_ACTIVE, drt/DRT_ALONE, drt/DRT_FAULTED, drt/DRT_NO_NETWORK, drt/DRT_STATUS, p2p.drt_status
ms.topic: enum
f1_keywords: 
 - "drt/DRT_STATUS"
dev_langs:
 - c++
req.header: drt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_STATUS
targetos: Windows
req.typenames: DRT_STATUS
req.redist: 
ms.custom: 19H1
---

# DRT_STATUS enumeration


## -description


The <b>DRT_STATUS</b> enumeration defines the status of a local DRT instance.


## -enum-fields




### -field DRT_ACTIVE

The local node is connected to the DRT mesh and participating in the DRT system. This is also an indication that remote nodes exist and are present in the cache of the local node.


### -field DRT_ALONE

The local node is participating in the DRT system, but is waiting for remote nodes to join the DRT mesh. This is an indication that remote nodes do not exist, or are not yet present in the cache of the local node.


### -field DRT_NO_NETWORK

The local node does not have network connectivity.


### -field DRT_FAULTED

A critical error has occurred in the local DRT instance. The <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtclose">DrtClose</a> function must be called, after which  an attempt to re-open the DRT can be made. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtclose">DrtClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>
 

 

