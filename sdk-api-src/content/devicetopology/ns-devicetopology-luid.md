---
UID: NS:devicetopology._LUID
title: LUID (devicetopology.h)
description: The LUID structure stores the video port identifier. This structure is stored in the PortId member of the KSJACK_SINK_INFORMATION structure.
helpviewer_keywords: ["*PLUID","LUID","LUID structure [Core Audio]","PLUID","PLUID structure pointer [Core Audio]","_LUID","coreaudio.luid","devicetopology/LUID","devicetopology/PLUID"]
old-location: coreaudio\luid.htm
tech.root: CoreAudio
ms.assetid: fce02fa7-ce96-417a-b389-cf19e1e3b91c
ms.date: 12/05/2018
ms.keywords: '*PLUID, LUID, LUID structure [Core Audio], PLUID, PLUID structure pointer [Core Audio], _LUID, coreaudio.luid, devicetopology/LUID, devicetopology/PLUID'
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
req.typenames: LUID, *PLUID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LUID
 - devicetopology/_LUID
 - PLUID
 - devicetopology/PLUID
 - LUID
 - devicetopology/LUID
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
 - LUID
---

# LUID structure


## -description

The <b>LUID</b> structure stores the video port identifier. This structure is stored in the <b>PortId</b> member of the  <a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_sink_information">KSJACK_SINK_INFORMATION</a> structure.

## -struct-fields

### -field LowPart

LowPart of the video port identifier.

### -field HighPart

HighPart of the video port identifier.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation">IKsJackSinkInformation::GetJackSinkInformation</a>