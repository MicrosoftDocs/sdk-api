---
UID: NS:mmddk.midiopendesc_tag
title: MIDIOPENDESC (mmddk.h)
description: The MIDIOPENDESC structure is a client-filled structure that provides information about how to open a MIDI device.
helpviewer_keywords: ["*LPMIDIOPENDESC","MIDIOPENDESC","MIDIOPENDESC structure [Audio Devices]","aud-prop_47abc723-0254-493a-9bc0-ac9faa73a2e8.xml","audio.midiopendesc","mmddk/MIDIOPENDESC"]
old-location: audio\midiopendesc.htm
tech.root: audio
ms.assetid: 7aacfd83-0188-4858-91e4-a6ce12a7e46d
ms.date: 12/05/2018
ms.keywords: '*LPMIDIOPENDESC, MIDIOPENDESC, MIDIOPENDESC structure [Audio Devices], aud-prop_47abc723-0254-493a-9bc0-ac9faa73a2e8.xml, audio.midiopendesc, mmddk/MIDIOPENDESC'
req.header: mmddk.h
req.include-header: Mmddk.h, Mmsystem.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows XP and later Windows operating systems.
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
req.typenames: MIDIOPENDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midiopendesc_tag
 - mmddk/midiopendesc_tag
 - MIDIOPENDESC
 - mmddk/MIDIOPENDESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmddk.h
api_name:
 - MIDIOPENDESC
---

# MIDIOPENDESC structure


## -description

The <code>MIDIOPENDESC</code> structure is a client-filled structure that provides information about how to open a MIDI device.

## -struct-fields

### -field hMidi

Specifies the handle that the client uses to reference the device. This handle is assigned by WINMM. Use this handle when you notify the client with the <a href="/previous-versions//ms708182(v=vs.85)">DriverCallback</a> function.

### -field dwCallback

Specifies either the address of a callback function, a window handle, or a task handle, depending on the flags that are specified in the dwParam2 parameter of the <a href="/previous-versions/windows/hardware/drivers/ff537541(v=vs.85)">MODM_OPEN</a> message. If this field contains a handle, it is contained in the low-order word.

### -field dwInstance

Specifies a pointer to a DWORD that contains instance information for the client. This instance information is returned to the client whenever the driver notifies the client by using the <b>DriverCallback</b> function.

### -field dnDevNode

Specifies a device node for the MIDI output device, if it is a Plug and Play (PnP) MIDI device.

### -field cIds

Specifies the number of stream identifiers, if a stream is open.

### -field rgIds

Specifies an array of device identifiers. The number of identifiers is given by the <b>cIds</b> member.

## -see-also

<a href="/previous-versions//ms708182(v=vs.85)">DriverCallback</a>