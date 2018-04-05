---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_CHANGE0_
title: IPSEC_SA_CONTEXT_CHANGE0_
author: windows-driver-content
description: Contains information about an IPsec security association (SA) context change.
old-location: fwp\ipsec_sa_context_change0.htm
old-project: FWP
ms.assetid: a81df783-72d8-4374-a3f8-44c3491a98db
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IPSEC_SA_CONTEXT_CHANGE0, IPSEC_SA_CONTEXT_CHANGE0 structure [Filtering], IPSEC_SA_CONTEXT_CHANGE0_, fwp.ipsec_sa_context_change0, ipsectypes/IPSEC_SA_CONTEXT_CHANGE0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IPSEC_SA_CONTEXT_CHANGE0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_SA_CONTEXT_CHANGE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_SA_CONTEXT_CHANGE0_ structure


## -description


The <b>IPSEC_SA_CONTEXT_CHANGE0</b> structure contains information about an IPsec security association (SA) context  change.


## -struct-fields




### -field changeType

Type: <b><a href="https://msdn.microsoft.com/3e179d08-2962-4196-9c7e-c16c9cddf489">IPSEC_SA_CONTEXT_EVENT_TYPE0</a></b>

The type of IPsec SA context change event.


### -field saContextId

Type: <b>UINT64</b>

Identifier of the IPsec SA context that changed.


## -see-also




<a href="https://msdn.microsoft.com/3e179d08-2962-4196-9c7e-c16c9cddf489">IPSEC_SA_CONTEXT_EVENT_TYPE0</a>
 

 

