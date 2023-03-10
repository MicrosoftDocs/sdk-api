---
UID: NS:dinputd.DIFFOBJECTATTRIBUTES
title: DIFFOBJECTATTRIBUTES (dinputd.h)
description: The DIFFOBJECTATTRIBUTES structure describes the information contained in the &quot;FFAttributes&quot; value of the registry key for each &quot;object&quot; on a force-feedback device.
helpviewer_keywords: ["*LPDIFFOBJECTATTRIBUTES","DIFFOBJECTATTRIBUTES","DIFFOBJECTATTRIBUTES structure [Human Input Devices]","di_ref_d710ceb3-0885-4f22-a4f3-326f24a1e29f.xml","dinputd/DIFFOBJECTATTRIBUTES","hid.diffobjectattributes"]
old-location: hid\diffobjectattributes.htm
tech.root: hid
ms.assetid: b5006cf1-619d-4521-b902-ab89a3f079a4
ms.date: 12/05/2018
ms.keywords: '*LPDIFFOBJECTATTRIBUTES, DIFFOBJECTATTRIBUTES, DIFFOBJECTATTRIBUTES structure [Human Input Devices], di_ref_d710ceb3-0885-4f22-a4f3-326f24a1e29f.xml, dinputd/DIFFOBJECTATTRIBUTES, hid.diffobjectattributes'
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
req.typenames: DIFFOBJECTATTRIBUTES, *LPDIFFOBJECTATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIFFOBJECTATTRIBUTES
 - dinputd/DIFFOBJECTATTRIBUTES
 - LPDIFFOBJECTATTRIBUTES
 - dinputd/LPDIFFOBJECTATTRIBUTES
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
 - DIFFOBJECTATTRIBUTES
---

# DIFFOBJECTATTRIBUTES structure


## -description

The DIFFOBJECTATTRIBUTES structure describes the information contained in the "FFAttributes" value of the registry key for each "object" on a force-feedback device. If the "FFAttributes" value is absent, then the object is assumed not to support force feedback.

## -struct-fields

### -field dwFFMaxForce

Specifies the magnitude of the maximum force that can be created by the actuator associated with this object. Force is expressed in Newtons and measured in relation to where the hand would be during <b>Normal</b> operation of the device. If this member is zero, the object is assumed not to support force feedback.

### -field dwFFForceResolution

Specifies the force resolution of the actuator associated with this object. The returned value represents the number of gradations, or subdivisions, of the maximum force that can be expressed by the force feedback system from 0 (no force) to maximum force.

