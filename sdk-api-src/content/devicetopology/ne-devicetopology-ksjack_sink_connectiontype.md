---
UID: NE:devicetopology.__MIDL___MIDL_itf_devicetopology_0000_0000_0010
title: KSJACK_SINK_CONNECTIONTYPE (devicetopology.h)
description: The KSJACK_SINK_CONNECTIONTYPE enumeration defines constants that specify the type of connection. These values are used in the KSJACK_SINK_INFORMATION structure that stores information about an audio jack sink.
helpviewer_keywords: ["KSJACK_SINK_CONNECTIONTYPE","KSJACK_SINK_CONNECTIONTYPE enumeration [Core Audio]","KSJACK_SINK_CONNECTIONTYPE_DISPLAYPORT","KSJACK_SINK_CONNECTIONTYPE_HDMI","coreaudio.ksjack_sink_connectiontype","devicetopology/KSJACK_SINK_CONNECTIONTYPE","devicetopology/KSJACK_SINK_CONNECTIONTYPE_DISPLAYPORT","devicetopology/KSJACK_SINK_CONNECTIONTYPE_HDMI"]
old-location: coreaudio\ksjack_sink_connectiontype.htm
tech.root: CoreAudio
ms.assetid: a1a9b0cf-b1bf-49df-a976-62f44fcf70ae
ms.date: 12/05/2018
ms.keywords: KSJACK_SINK_CONNECTIONTYPE, KSJACK_SINK_CONNECTIONTYPE enumeration [Core Audio], KSJACK_SINK_CONNECTIONTYPE_DISPLAYPORT, KSJACK_SINK_CONNECTIONTYPE_HDMI, coreaudio.ksjack_sink_connectiontype, devicetopology/KSJACK_SINK_CONNECTIONTYPE, devicetopology/KSJACK_SINK_CONNECTIONTYPE_DISPLAYPORT, devicetopology/KSJACK_SINK_CONNECTIONTYPE_HDMI
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KSJACK_SINK_CONNECTIONTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_devicetopology_0000_0000_0010
 - devicetopology/__MIDL___MIDL_itf_devicetopology_0000_0000_0010
 - KSJACK_SINK_CONNECTIONTYPE
 - devicetopology/KSJACK_SINK_CONNECTIONTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - KSJACK_SINK_CONNECTIONTYPE
---

# KSJACK_SINK_CONNECTIONTYPE enumeration


## -description

The <b>KSJACK_SINK_CONNECTIONTYPE</b> enumeration defines constants that specify the type of connection. These values are used in  the <a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_sink_information">KSJACK_SINK_INFORMATION</a> structure that stores information about an audio jack sink.

## -enum-fields

### -field KSJACK_SINK_CONNECTIONTYPE_HDMI:0

High-Definition Multimedia Interface (HDMI) connection.

### -field KSJACK_SINK_CONNECTIONTYPE_DISPLAYPORT

Display port.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation">IKsJackSinkInformation::GetJackSinkInformation</a>



<a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_sink_information">KSJACK_SINK_INFORMATION</a>
