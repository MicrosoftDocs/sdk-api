---
UID: NS:dinputd.DIJOYUSERVALUES
title: DIJOYUSERVALUES (dinputd.h)
description: The DIJOYUSERVALUES structure contains information about the user's joystick settings.
helpviewer_keywords: ["*LPDIJOYUSERVALUES","DIJOYUSERVALUES","DIJOYUSERVALUES structure [Human Input Devices]","di_ref_bbcc635e-bb11-4ddb-9e15-0b84b4d28ea5.xml","dinputd/DIJOYUSERVALUES","hid.dijoyuservalues"]
old-location: hid\dijoyuservalues.htm
tech.root: hid
ms.assetid: 15424c18-c9ae-4058-97b4-f55b56daea72
ms.date: 12/05/2018
ms.keywords: '*LPDIJOYUSERVALUES, DIJOYUSERVALUES, DIJOYUSERVALUES structure [Human Input Devices], di_ref_bbcc635e-bb11-4ddb-9e15-0b84b4d28ea5.xml, dinputd/DIJOYUSERVALUES, hid.dijoyuservalues'
req.header: dinputd.h
req.include-header: 
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
req.typenames: DIJOYUSERVALUES, *LPDIJOYUSERVALUES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIJOYUSERVALUES
 - dinputd/DIJOYUSERVALUES
 - LPDIJOYUSERVALUES
 - dinputd/LPDIJOYUSERVALUES
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
 - DIJOYUSERVALUES
---

# DIJOYUSERVALUES structure


## -description

The <b>DIJOYUSERVALUES</b> structure contains information about the user's joystick settings.

## -struct-fields

### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used.

### -field ruv

Joystick user configuration. In addition to the fields contained in the mmddk.h header file, the previously unused <b>jrvRanges.jpCenter</b> field contains the user saturation levels for each axis. A control panel application sets the dead zone and saturation values based on the values set by the end-user during calibration or fine-tuning. Dead zone can be interpreted as "sensitivity in the center" and saturation can be interpreted as "sensitivity along the edges".

### -field wszGlobalDriver

The global port driver.

### -field wszGameportEmulator

Unused.

