---
UID: NE:drt.drt_status_tag
title: drt_status_tag
author: windows-sdk-content
description: The DRT_STATUS enumeration defines the status of a local DRT instance.
old-location: p2p\drt_status.htm
old-project: p2psdk
ms.assetid: 4bd81191-862c-4537-9c90-4b9fec270a16
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRT_ACTIVE, DRT_ALONE, DRT_FAULTED, DRT_NO_NETWORK, DRT_STATUS, DRT_STATUS enumeration [Peer Networking], drt/DRT_ACTIVE, drt/DRT_ALONE, drt/DRT_FAULTED, drt/DRT_NO_NETWORK, drt/DRT_STATUS, drt_status_tag, p2p.drt_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: drt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DRT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# drt_status_tag enumeration


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

A critical error has occurred in the local DRT instance. The <a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a> function must be called, after which  an attempt to re-open the DRT can be made. 


## -see-also




<a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 

