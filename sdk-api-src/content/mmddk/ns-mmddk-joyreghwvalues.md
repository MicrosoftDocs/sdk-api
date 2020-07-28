---
UID: NS:mmddk.joyreghwvalues_tag
title: JOYREGHWVALUES (mmddk.h)
description: The JOYREGHWVALUES structure contains the range of values returned by the hardware (filled in by calibration).
helpviewer_keywords: ["*LPJOYREGHWVALUES","FAR *LPJOYREGHWVALUES","FAR *LPJOYREGHWVALUES structure [Human Input Devices]","JOYREGHWVALUES","JOYREGHWVALUES structure [Human Input Devices]","di_ref_bd51a1ee-82e2-417f-81a1-9732931706a3.xml","hid.joyreghwvalues","mmddk/FAR *LPJOYREGHWVALUES","mmddk/JOYREGHWVALUES"]
old-location: hid\joyreghwvalues.htm
tech.root: hid
ms.assetid: cd59611f-7bf2-4bba-80dc-f54c815af3e6
ms.date: 12/05/2018
ms.keywords: '*LPJOYREGHWVALUES, FAR *LPJOYREGHWVALUES, FAR *LPJOYREGHWVALUES structure [Human Input Devices], JOYREGHWVALUES, JOYREGHWVALUES structure [Human Input Devices], di_ref_bd51a1ee-82e2-417f-81a1-9732931706a3.xml, hid.joyreghwvalues, mmddk/FAR *LPJOYREGHWVALUES, mmddk/JOYREGHWVALUES'
f1_keywords:
- mmddk/JOYREGHWVALUES
dev_langs:
- c++
req.header: mmddk.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mmddk.h
api_name:
- JOYREGHWVALUES
targetos: Windows
req.typenames: JOYREGHWVALUES, *LPJOYREGHWVALUES
req.redist: 
ms.custom: 19H1
---

# JOYREGHWVALUES structure


## -description


The <b>JOYREGHWVALUES</b> structure contains the range of values returned by the hardware (filled in by calibration).


## -struct-fields




### -field jrvHardware

The values returned by the hardware.


### -field dwPOVValues

The point-of-view (POV) values returned by the hardware.


### -field dwCalFlags

What has been calibrated.

