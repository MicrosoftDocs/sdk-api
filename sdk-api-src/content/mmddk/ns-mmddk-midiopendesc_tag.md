---
UID: NS:mmddk.midiopendesc_tag
title: midiopendesc_tag
author: windows-sdk-content
description: The MIDIOPENDESC structure is a client-filled structure that provides information about how to open a MIDI device.
old-location: audio\midiopendesc.htm
old-project: audio
ms.assetid: 7aacfd83-0188-4858-91e4-a6ce12a7e46d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*LPMIDIOPENDESC, MIDIOPENDESC, MIDIOPENDESC structure [Audio Devices], aud-prop_47abc723-0254-493a-9bc0-ac9faa73a2e8.xml, audio.midiopendesc, midiopendesc_tag, mmddk/MIDIOPENDESC"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmddk.h
req.include-header: Mmddk.h, Mmsystem.h, Windows.h
req.redist: 
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
tech.root: 
req.typenames: MIDIOPENDESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmddk.h
api_name:
 - MIDIOPENDESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# midiopendesc_tag structure


## -description


The <code>MIDIOPENDESC</code> structure is a client-filled structure that provides information about how to open a MIDI device.


## -struct-fields




### -field hMidi

Specifies the handle that the client uses to reference the device. This handle is assigned by WINMM. Use this handle when you notify the client with the <a href="http://go.microsoft.com/fwlink/p/?linkid=142261">DriverCallback</a> function.


### -field dwCallback

Specifies either the address of a callback function, a window handle, or a task handle, depending on the flags that are specified in the dwParam2 parameter of the <a href="https://msdn.microsoft.com/9a0b4bb8-15fd-48d4-8840-c0c7b4a5a460">MODM_OPEN</a> message. If this field contains a handle, it is contained in the low-order word.


### -field dwInstance

Specifies a pointer to a DWORD that contains instance information for the client. This instance information is returned to the client whenever the driver notifies the client by using the <b>DriverCallback</b> function.


### -field dnDevNode

Specifies a device node for the MIDI output device, if it is a Plug and Play (PnP) MIDI device.


### -field cIds

Specifies the number of stream identifiers, if a stream is open.


### -field rgIds

Specifies an array of device identifiers. The number of identifiers is given by the <b>cIds</b> member.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=142261">DriverCallback</a>
 

 

