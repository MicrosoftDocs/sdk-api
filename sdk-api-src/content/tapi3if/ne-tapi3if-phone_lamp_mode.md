---
UID: NE:tapi3if.PHONE_LAMP_MODE
title: PHONE_LAMP_MODE (tapi3if.h)
description: The PHONE_LAMP_MODE enum provides indicators of a phone lamp's status.
helpviewer_keywords: ["LM_BROKENFLUTTER","LM_DUMMY","LM_FLASH","LM_FLUTTER","LM_OFF","LM_STEADY","LM_UNKNOWN","LM_WINK","PHONE_LAMP_MODE","PHONE_LAMP_MODE enumeration [TAPI 2.2]","_tapi3_phone_lamp_mode","tapi3.phone_lamp_mode","tapi3if/LM_BROKENFLUTTER","tapi3if/LM_DUMMY","tapi3if/LM_FLASH","tapi3if/LM_FLUTTER","tapi3if/LM_OFF","tapi3if/LM_STEADY","tapi3if/LM_UNKNOWN","tapi3if/LM_WINK","tapi3if/PHONE_LAMP_MODE"]
old-location: tapi3\phone_lamp_mode.htm
tech.root: tapi3
ms.assetid: cb971936-269c-4e59-bfc1-a3edc977ceb5
ms.date: 12/05/2018
ms.keywords: LM_BROKENFLUTTER, LM_DUMMY, LM_FLASH, LM_FLUTTER, LM_OFF, LM_STEADY, LM_UNKNOWN, LM_WINK, PHONE_LAMP_MODE, PHONE_LAMP_MODE enumeration [TAPI 2.2], _tapi3_phone_lamp_mode, tapi3.phone_lamp_mode, tapi3if/LM_BROKENFLUTTER, tapi3if/LM_DUMMY, tapi3if/LM_FLASH, tapi3if/LM_FLUTTER, tapi3if/LM_OFF, tapi3if/LM_STEADY, tapi3if/LM_UNKNOWN, tapi3if/LM_WINK, tapi3if/PHONE_LAMP_MODE
req.header: tapi3if.h
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
req.typenames: PHONE_LAMP_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONE_LAMP_MODE
 - tapi3if/PHONE_LAMP_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - PHONE_LAMP_MODE
---

# PHONE_LAMP_MODE enumeration


## -description

The 
<b>PHONE_LAMP_MODE</b> enum provides indicators of a phone lamp's status.

## -enum-fields

### -field LM_DUMMY:0x1

The lamp identifier has no corresponding lamp.

### -field LM_OFF:0x2

The lamp is off.

### -field LM_STEADY:0x4

The lamp is on steadily.

### -field LM_WINK:0x8

The lamp is winking, which means on and off at a normal rate.

### -field LM_FLASH:0x10

The lamp is flashing, which means a slow on and off.

### -field LM_FLUTTER:0x20

The lamp is fluttering, which means a fast on and off.

### -field LM_BROKENFLUTTER:0x40

The lamp is flashing, which means superposition of a flash and flutter.

### -field LM_UNKNOWN:0x80

The lamp mode is not known.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_lampmode">ITPhone::get_LampMode</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_lampmode">ITPhone::put_LampMode</a>
