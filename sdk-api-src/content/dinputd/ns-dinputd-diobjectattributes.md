---
UID: NS:dinputd.DIOBJECTATTRIBUTES
title: DIOBJECTATTRIBUTES (dinputd.h)
description: The DIOBJECTATTRIBUTES structure describes the information contained in the &quot;Attributes&quot; value of the registry key for each &quot;object&quot; on a device. If the &quot;Attributes&quot; value is absent, then default attributes are used.
helpviewer_keywords: ["*LPDIOBJECTATTRIBUTES","DIOBJECTATTRIBUTES","DIOBJECTATTRIBUTES structure [Human Input Devices]","di_ref_c88696fe-68b4-4b0e-88dd-96be38e0bdd4.xml","dinputd/DIOBJECTATTRIBUTES","hid.diobjectattributes"]
old-location: hid\diobjectattributes.htm
tech.root: hid
ms.assetid: 773bf345-5bdd-4b05-b291-1e844bdb9cf0
ms.date: 12/05/2018
ms.keywords: '*LPDIOBJECTATTRIBUTES, DIOBJECTATTRIBUTES, DIOBJECTATTRIBUTES structure [Human Input Devices], di_ref_c88696fe-68b4-4b0e-88dd-96be38e0bdd4.xml, dinputd/DIOBJECTATTRIBUTES, hid.diobjectattributes'
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DIOBJECTATTRIBUTES, *LPDIOBJECTATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIOBJECTATTRIBUTES
 - dinputd/DIOBJECTATTRIBUTES
 - LPDIOBJECTATTRIBUTES
 - dinputd/LPDIOBJECTATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIOBJECTATTRIBUTES
---

# DIOBJECTATTRIBUTES structure


## -description

The DIOBJECTATTRIBUTES structure describes the information contained in the "Attributes" value of the registry key for each "object" on a device. If the "Attributes" value is absent, then default attributes are used.

## -struct-fields

### -field dwFlags

 There may be zero, one, or more of the following flags: 





#### DIDOI_FFACTUATOR

Indicates that the object can have force feedback effects applied to it. 



#### DIDOI_FFEFFECTTRIGGER

Indicates that the object can trigger playback of force feedback effects. 



#### DIDOI_ASPECTPOSITION

Indicates that the object reports position information. 



#### DIDOI_ASPECTVELOCITY

Indicates that the object reports velocity information. 



#### DIDOI_ASPECTACCEL

Indicates that the object reports acceleration information. 



#### DIDOI_ASPECTFORCE

Indicates that the object reports force information. 



#### DIDOI_ASPECTMASK

Indicates the bits that are used to report aspect information. An object can represent, at most, one aspect. 



#### DIDOI_POLLED

Indicates that the object must be explicitly polled in order for data to be retrieved from it. If this flag is not set, then data for the object is interrupt-driven.

### -field wUsagePage

Specifies the HID usage page to associate with the object.

### -field wUsage

Specifies the HID usage to associate with the object.

