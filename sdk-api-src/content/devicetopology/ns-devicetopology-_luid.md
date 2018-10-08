---
UID: NS:devicetopology._LUID
title: "_LUID"
author: windows-sdk-content
description: The LUID structure stores the video port identifier. This structure is stored in the PortId member of the KSJACK_SINK_INFORMATION structure.
old-location: coreaudio\luid.htm
tech.root: CoreAudio
ms.assetid: fce02fa7-ce96-417a-b389-cf19e1e3b91c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PLUID, LUID, LUID structure [Core Audio], PLUID, PLUID structure pointer [Core Audio], _LUID, coreaudio.luid, devicetopology/LUID, devicetopology/PLUID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - LUID
product: Windows
targetos: Windows
req.typenames: LUID, *PLUID
req.redist: 
---

# _LUID structure


## -description


The <b>LUID</b> structure stores the video port identifier. This structure is stored in the <b>PortId</b> member of the  <a href="https://msdn.microsoft.com/ee7211d8-a34f-40c9-9925-7bb40792bae9">KSJACK_SINK_INFORMATION</a> structure.


## -struct-fields




### -field LowPart

LowPart of the video port identifier.


### -field HighPart

HighPart of the video port identifier. 


## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/ca4165ce-433a-4a8f-9853-bbe812de90ca">IKsJackSinkInformation::GetJackSinkInformation</a>
 

 

