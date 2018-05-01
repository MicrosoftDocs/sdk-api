---
UID: NE:mprapi._RAS_PORT_CONDITION
title: "_RAS_PORT_CONDITION"
author: windows-driver-content
description: The RAS_PORT_CONDITION enumerated type specifies information regarding the connection condition of a given RAS port.
old-location: rras\ras_port_condition.htm
old-project: RRAS
ms.assetid: 86bcca08-97c5-404c-b5d9-a90d93f26e00
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: RAS_PORT_AUTHENTICATED, RAS_PORT_AUTHENTICATING, RAS_PORT_CALLING_BACK, RAS_PORT_CONDITION, RAS_PORT_CONDITION enumeration [RAS], RAS_PORT_DISCONNECTED, RAS_PORT_INITIALIZING, RAS_PORT_LISTENING, RAS_PORT_NON_OPERATIONAL, _RAS_PORT_CONDITION, _mpr_ras_port_condition, mprapi/RAS_PORT_AUTHENTICATED, mprapi/RAS_PORT_AUTHENTICATING, mprapi/RAS_PORT_CALLING_BACK, mprapi/RAS_PORT_CONDITION, mprapi/RAS_PORT_DISCONNECTED, mprapi/RAS_PORT_INITIALIZING, mprapi/RAS_PORT_LISTENING, mprapi/RAS_PORT_NON_OPERATIONAL, rras.ras_port_condition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RAS_PORT_CONDITION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	RAS_PORT_CONDITION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _RAS_PORT_CONDITION enumeration


## -description


The 
<b>RAS_PORT_CONDITION</b> enumerated type specifies information regarding the connection condition of a given RAS port.


## -enum-fields




### -field RAS_PORT_NON_OPERATIONAL

The port is not operational.


### -field RAS_PORT_DISCONNECTED

The port is disconnected.


### -field RAS_PORT_CALLING_BACK

The port is in the process of a call back.


### -field RAS_PORT_LISTENING

The port is listening for incoming calls.


### -field RAS_PORT_AUTHENTICATING

The port is authenticating a user.


### -field RAS_PORT_AUTHENTICATED

The port has authenticated a user.


### -field RAS_PORT_INITIALIZING

The port is initializing.


## -see-also




<a href="https://msdn.microsoft.com/6d044d35-5c50-4c30-89b4-8963d3b85673">RAS Administration Enumerated Types</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

