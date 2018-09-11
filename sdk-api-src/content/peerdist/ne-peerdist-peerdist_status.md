---
UID: NE:peerdist.PEERDIST_STATUS
title: PEERDIST_STATUS
author: windows-sdk-content
description: PEERDIST_STATUS enumeration defines the possible status values of the Peer Distribution service.
old-location: p2p\peerdist_status.htm
tech.root: p2psdk
ms.assetid: d693dc1c-39ce-4a2b-b769-9d370abc3d3c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PEERDIST_STATUS, PEERDIST_STATUS enumeration [Peer Networking], PEERDIST_STATUS_AVAILABLE, PEERDIST_STATUS_DISABLED, PEERDIST_STATUS_UNAVAILABLE, p2p.peerdist_status, peerdist/PEERDIST_STATUS, peerdist/PEERDIST_STATUS_AVAILABLE, peerdist/PEERDIST_STATUS_DISABLED, peerdist/PEERDIST_STATUS_UNAVAILABLE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_STATUS
product: Windows
targetos: Windows
req.typenames: PEERDIST_STATUS
req.redist: 
---

# PEERDIST_STATUS enumeration


## -description


The <b>PEERDIST_STATUS</b> enumeration defines the possible status values of the Peer Distribution service.


## -enum-fields




### -field PEERDIST_STATUS_DISABLED

The service is disabled by Group Policy or according to configuration parameters.


### -field PEERDIST_STATUS_UNAVAILABLE

The service is not ready to process the request.


### -field PEERDIST_STATUS_AVAILABLE

The Peer Distribution service  is available and ready to process  requests.


## -see-also




<a href="https://msdn.microsoft.com/1ab188cc-db79-49b2-977f-0b8fccf7f274">PeerDistGetStatus</a>
 

 

