---
UID: NE:drt.drt_security_mode_tag
title: DRT_SECURITY_MODE
author: windows-sdk-content
description: The DRT_SECURITY_MODE enumeration defines possible security modes for the DRT. The security mode is specified by a field of the DRT_SETTINGS structure.
old-location: p2p\drt_security_mode.htm
tech.root: P2PSdk
ms.assetid: 652942a3-94cd-466c-bf7c-80e87ba692c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRT_SECURE_CONFIDENTIALPAYLOAD, DRT_SECURE_MEMBERSHIP, DRT_SECURE_RESOLVE, DRT_SECURITY_MODE, DRT_SECURITY_MODE enumeration [Distributed Routing Tables], drt/DRT_SECURE_CONFIDENTIALPAYLOAD, drt/DRT_SECURE_MEMBERSHIP, drt/DRT_SECURE_RESOLVE, drt/DRT_SECURITY_MODE, p2p.drt_security_mode
ms.topic: enum
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
 - DRT_SECURITY_MODE
product: Windows
targetos: Windows
req.typenames: DRT_SECURITY_MODE
req.redist: 
---

# DRT_SECURITY_MODE enumeration


## -description


The <b>DRT_SECURITY_MODE</b> enumeration defines possible security modes for the DRT. The security mode is specified by a field of the <a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a> structure.


## -enum-fields




### -field DRT_SECURE_RESOLVE

Nodes must authenticate the keys they publish. Nodes are not required to authenticate themselves when performing searches.


### -field DRT_SECURE_MEMBERSHIP

Nodes must authenticate the keys they publish. Nodes must also authenticate themselves when performing searches. Unauthorized nodes cannot search for  keys and cannot retrieve the data associated with published keys.


### -field DRT_SECURE_CONFIDENTIALPAYLOAD

Nodes must authenticate the keys they publish. Nodes must also authenticate themselves when performing searches. Encryption is required for all data associated with published keys prior to transmission between DRT nodes. Unauthorized nodes cannot search for keys, cannot retrieve the data associated with published keys, and cannot retrieve data by observing network traffic between other DRT nodes.


## -remarks



The more secure a DRT security mode, the more of a computational load exists for nodes participating in the DRT. More bandwidth is also consumed.



