---
UID: NS:drt._DRT_ADDRESS
title: "_DRT_ADDRESS"
author: windows-sdk-content
description: DRT_ADDRESS structure contains endpoint information about a DRT node that participated in a search. This information is intended for use in debugging connectivity problems.
old-location: p2p\drt_address.htm
tech.root: P2PSdk
ms.assetid: d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDRT_ADDRESS, DRT_ADDRESS, DRT_ADDRESS structure [Peer Networking], PDRT_ADDRESS, PDRT_ADDRESS structure pointer [Peer Networking], _DRT_ADDRESS, drt/DRT_ADDRESS, drt/PDRT_ADDRESS, p2p.drt_address"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - DRT_ADDRESS
product: Windows
targetos: Windows
req.typenames: DRT_ADDRESS, *PDRT_ADDRESS
req.redist: 
---

# _DRT_ADDRESS structure


## -description


The <b>DRT_ADDRESS</b> structure contains endpoint information about a DRT node that participated in a search.  This information is intended for use in debugging connectivity problems.


## -struct-fields




### -field socketAddress

Contains the endpoint on which the DRT protocol is listening on the remote node.


### -field flags

Holds information explaining how this node behaved in the key lookup.


### -field nearness

Contains the number of bits that the key published by this node shares in common with the target key in the search.


### -field latency

Round trip time to this node.


## -see-also




<a href="https://msdn.microsoft.com/a795dff7-4182-42ad-b14b-142a6c1312c7">DRT_ADDRESS_LIST</a>
 

 

