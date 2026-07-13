---
UID: NE:tapi3if.PHONECAPS_LONG
title: PHONECAPS_LONG (tapi3if.h)
description: The PHONECAPS_LONG enum is used by methods that set or get phone capabilities described by a long value.
helpviewer_keywords: ["PCL_DISPLAYNUMCOLUMNS","PCL_DISPLAYNUMROWS","PCL_GENERICPHONE","PCL_HANDSETHOOKSWITCHMODES","PCL_HEADSETHOOKSWITCHMODES","PCL_HOOKSWITCHES","PCL_NUMBUTTONLAMPS","PCL_NUMRINGMODES","PCL_SPEAKERPHONEHOOKSWITCHMODES","PHONECAPS_LONG","PHONECAPS_LONG enumeration [TAPI 2.2]","_tapi3_phonecaps_long","tapi3.phonecaps_long","tapi3if/PCL_DISPLAYNUMCOLUMNS","tapi3if/PCL_DISPLAYNUMROWS","tapi3if/PCL_GENERICPHONE","tapi3if/PCL_HANDSETHOOKSWITCHMODES","tapi3if/PCL_HEADSETHOOKSWITCHMODES","tapi3if/PCL_HOOKSWITCHES","tapi3if/PCL_NUMBUTTONLAMPS","tapi3if/PCL_NUMRINGMODES","tapi3if/PCL_SPEAKERPHONEHOOKSWITCHMODES","tapi3if/PHONECAPS_LONG"]
old-location: tapi3\phonecaps_long.htm
tech.root: tapi3
ms.assetid: 7a73d5ff-d08a-46e6-b4ad-4f3b973967a7
ms.date: 12/05/2018
ms.keywords: PCL_DISPLAYNUMCOLUMNS, PCL_DISPLAYNUMROWS, PCL_GENERICPHONE, PCL_HANDSETHOOKSWITCHMODES, PCL_HEADSETHOOKSWITCHMODES, PCL_HOOKSWITCHES, PCL_NUMBUTTONLAMPS, PCL_NUMRINGMODES, PCL_SPEAKERPHONEHOOKSWITCHMODES, PHONECAPS_LONG, PHONECAPS_LONG enumeration [TAPI 2.2], _tapi3_phonecaps_long, tapi3.phonecaps_long, tapi3if/PCL_DISPLAYNUMCOLUMNS, tapi3if/PCL_DISPLAYNUMROWS, tapi3if/PCL_GENERICPHONE, tapi3if/PCL_HANDSETHOOKSWITCHMODES, tapi3if/PCL_HEADSETHOOKSWITCHMODES, tapi3if/PCL_HOOKSWITCHES, tapi3if/PCL_NUMBUTTONLAMPS, tapi3if/PCL_NUMRINGMODES, tapi3if/PCL_SPEAKERPHONEHOOKSWITCHMODES, tapi3if/PHONECAPS_LONG
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
req.typenames: PHONECAPS_LONG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PHONECAPS_LONG
 - tapi3if/PHONECAPS_LONG
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
 - PHONECAPS_LONG
---

# PHONECAPS_LONG enumeration


## -description

The 
<b>PHONECAPS_LONG</b> enum is used by methods that set or get phone capabilities described by a long value.

## -enum-fields

### -field PCL_HOOKSWITCHES:0

Specifies the hookswitch devices available using one or more members of the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_device">PHONE_HOOK_SWITCH_DEVICE</a> enum.

### -field PCL_HANDSETHOOKSWITCHMODES

Specifies the handset hook switch modes.

### -field PCL_HEADSETHOOKSWITCHMODES

Specifies the headset hook switch modes.

### -field PCL_SPEAKERPHONEHOOKSWITCHMODES

Specifies the speakerphone hook switch modes.

### -field PCL_DISPLAYNUMROWS

Specifies the number of rows in a phone display device.

### -field PCL_DISPLAYNUMCOLUMNS

Specifies the number of columns in a phone display device.

### -field PCL_NUMRINGMODES

Specifies the number of ring modes. 




If a USB phone returns zero for this value, the phone typically does not have a ringer device. The ringing sound plays on the default audio device for the system; for example, on sound card speakers.

### -field PCL_NUMBUTTONLAMPS

Specifies the number of button lamps.

### -field PCL_GENERICPHONE

Specifies whether the phone is generic: a value of one indicates it is, a value of zero indicates it is not. 




A generic phone is a phone device that declares itself as available on all addresses that support audio terminals. For example, a USB phone is generic, because it is not tied to a specific TAPI address.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_phonecapslong">ITPhone::get_PhoneCapsLong</a>
