---
UID: NS:dinputd.DIFFDEVICEATTRIBUTES
title: DIFFDEVICEATTRIBUTES (dinputd.h)
description: The DIFFDEVICEATTRIBUTES structure describes the information contained in the &quot;Attributes&quot; value of the OEMForceFeedback registry key.
helpviewer_keywords: ["*LPDIFFDEVICEATTRIBUTES","DIFFDEVICEATTRIBUTES","DIFFDEVICEATTRIBUTES structure [Human Input Devices]","di_ref_64e91043-878c-49d2-9e1a-b16bb5ed22b6.xml","dinputd/DIFFDEVICEATTRIBUTES","hid.diffdeviceattributes"]
old-location: hid\diffdeviceattributes.htm
tech.root: hid
ms.assetid: d4011b83-955f-4af8-85f7-a901dc67c8ec
ms.date: 12/05/2018
ms.keywords: '*LPDIFFDEVICEATTRIBUTES, DIFFDEVICEATTRIBUTES, DIFFDEVICEATTRIBUTES structure [Human Input Devices], di_ref_64e91043-878c-49d2-9e1a-b16bb5ed22b6.xml, dinputd/DIFFDEVICEATTRIBUTES, hid.diffdeviceattributes'
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
req.typenames: DIFFDEVICEATTRIBUTES, *LPDIFFDEVICEATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIFFDEVICEATTRIBUTES
 - dinputd/DIFFDEVICEATTRIBUTES
 - LPDIFFDEVICEATTRIBUTES
 - dinputd/LPDIFFDEVICEATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dinputd.h
api_name:
 - DIFFDEVICEATTRIBUTES
---

# DIFFDEVICEATTRIBUTES structure


## -description

The DIFFDEVICEATTRIBUTES structure describes the information contained in the "Attributes" value of the <b>OEMForceFeedback</b> registry key.

## -struct-fields

### -field dwFlags

Reserved for future use. This member must be set to zero.

### -field dwFFSamplePeriod

Specifies the minimum time between playback of force commands, in microseconds.

### -field dwFFMinTimeResolution

Specifies the minimum amount of time that the device can resolve, in microseconds. The device rounds any time values to the nearest supported increment. For example, if the value of <b>dwFFMinTimeResolution</b> is 1000, then the device would round any times to the nearest millisecond.

