---
UID: NS:dinput.DIEFFESCAPE
title: DIEFFESCAPE (dinput.h)
description: The DIEFFESCAPE structure passes hardware-specific data directly to the device driver.
helpviewer_keywords: ["*LPDIEFFESCAPE","DIEFFESCAPE","DIEFFESCAPE structure [Human Input Devices]","DIEFFESCAPE","*LPDIEFFESCAPE","DIEFFESCAPE","*LPDIEFFESCAPE structure [Human Input Devices]","di_ref_b6b4b11a-a6ad-4467-a2c6-1c69047dec2f.xml","dinput/DIEFFESCAPE","hid.dieffescape"]
old-location: hid\dieffescape.htm
tech.root: hid
ms.assetid: 97d452b2-aa25-46a9-a755-dc835270c818
ms.date: 12/05/2018
ms.keywords: '*LPDIEFFESCAPE, DIEFFESCAPE, DIEFFESCAPE structure [Human Input Devices], DIEFFESCAPE,*LPDIEFFESCAPE, DIEFFESCAPE,*LPDIEFFESCAPE structure [Human Input Devices], di_ref_b6b4b11a-a6ad-4467-a2c6-1c69047dec2f.xml, dinput/DIEFFESCAPE, hid.dieffescape'
req.header: dinput.h
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
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIEFFESCAPE
 - dinput/DIEFFESCAPE
 - LPDIEFFESCAPE
 - dinput/LPDIEFFESCAPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinput.h
api_name:
 - DIEFFESCAPE, *LPDIEFFESCAPE
---

# DIEFFESCAPE structure


## -description

The <b>DIEFFESCAPE</b> structure passes hardware-specific data directly to the device driver.

## -struct-fields

### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used.

### -field dwCommand

Specifies a driver-specific command number. Contact the hardware vendor for a list of valid commands and their parameters.

### -field lpvInBuffer

Points to the buffer containing the data required to perform the operation.

### -field cbInBuffer

Specifies the size, in bytes, of the <b>lpvInBuffer</b> buffer.

### -field lpvOutBuffer

Points to the buffer in which the operation's output data is returned.

### -field cbOutBuffer

On entry, specifies the size, in bytes, of the <b>lpvOutBuffer</b> buffer. On exit, specifies the number of bytes actually produced by the command.

