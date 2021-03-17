---
UID: NE:mprapi._RAS_PORT_CONDITION
title: RAS_PORT_CONDITION (mprapi.h)
description: The RAS_PORT_CONDITION enumerated type specifies information regarding the connection condition of a given RAS port.
helpviewer_keywords: ["RAS_PORT_AUTHENTICATED","RAS_PORT_AUTHENTICATING","RAS_PORT_CALLING_BACK","RAS_PORT_CONDITION","RAS_PORT_CONDITION enumeration [RAS]","RAS_PORT_DISCONNECTED","RAS_PORT_INITIALIZING","RAS_PORT_LISTENING","RAS_PORT_NON_OPERATIONAL","_mpr_ras_port_condition","mprapi/RAS_PORT_AUTHENTICATED","mprapi/RAS_PORT_AUTHENTICATING","mprapi/RAS_PORT_CALLING_BACK","mprapi/RAS_PORT_CONDITION","mprapi/RAS_PORT_DISCONNECTED","mprapi/RAS_PORT_INITIALIZING","mprapi/RAS_PORT_LISTENING","mprapi/RAS_PORT_NON_OPERATIONAL","rras.ras_port_condition"]
old-location: rras\ras_port_condition.htm
tech.root: RRAS
ms.assetid: 86bcca08-97c5-404c-b5d9-a90d93f26e00
ms.date: 12/05/2018
ms.keywords: RAS_PORT_AUTHENTICATED, RAS_PORT_AUTHENTICATING, RAS_PORT_CALLING_BACK, RAS_PORT_CONDITION, RAS_PORT_CONDITION enumeration [RAS], RAS_PORT_DISCONNECTED, RAS_PORT_INITIALIZING, RAS_PORT_LISTENING, RAS_PORT_NON_OPERATIONAL, _mpr_ras_port_condition, mprapi/RAS_PORT_AUTHENTICATED, mprapi/RAS_PORT_AUTHENTICATING, mprapi/RAS_PORT_CALLING_BACK, mprapi/RAS_PORT_CONDITION, mprapi/RAS_PORT_DISCONNECTED, mprapi/RAS_PORT_INITIALIZING, mprapi/RAS_PORT_LISTENING, mprapi/RAS_PORT_NON_OPERATIONAL, rras.ras_port_condition
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RAS_PORT_CONDITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_PORT_CONDITION
 - mprapi/_RAS_PORT_CONDITION
 - RAS_PORT_CONDITION
 - mprapi/RAS_PORT_CONDITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - RAS_PORT_CONDITION
---

# RAS_PORT_CONDITION enumeration


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

<a href="/windows/desktop/RRAS/ras-administration-enumerations">RAS Administration Enumerated Types</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>