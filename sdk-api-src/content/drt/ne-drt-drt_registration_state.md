---
UID: NE:drt._DRT_REGISTRATION_STATE
title: DRT_REGISTRATION_STATE (drt.h)
author: windows-sdk-content
description: The DRT_REGISTRATION_STATE enumeration defines the set of legal states for a registered key.
old-location: p2p\drt_registration_state.htm
tech.root: P2PSdk
ms.assetid: 4c383efb-fedb-4f6f-9ae7-48fdf42887ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDRT_REGISTRATION_STATE, DRT_REGISTRATION_STATE, DRT_REGISTRATION_STATE enumeration [Distributed Routing Tables], DRT_REGISTRATION_STATE_UNRESOLVEABLE, drt/DRT_REGISTRATION_STATE, drt/DRT_REGISTRATION_STATE_UNRESOLVEABLE, p2p.drt_registration_state"
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
 - DRT_REGISTRATION_STATE
product: Windows
targetos: Windows
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
req.redist: 
---

# DRT_REGISTRATION_STATE enumeration


## -description


The <b>DRT_REGISTRATION_STATE</b> enumeration defines the set of legal states for a registered key.


## -enum-fields




### -field DRT_REGISTRATION_STATE_UNRESOLVEABLE

The locally registered key is no longer resolvable by other nodes. The Distributed Routing Table signals this state when the local security provider is unable to generate an authentication token for the locally registered key. 

For example, if the Derived Key Security Provider is used, this state is signaled when the certificate used to authenticate expires.

