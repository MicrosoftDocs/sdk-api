---
UID: NS:devicetopology._tagKSJACK_DESCRIPTION2
title: "_tagKSJACK_DESCRIPTION2"
author: windows-sdk-content
description: The KSJACK_DESCRIPTION2 structure describes an audio jack.To get the description of an audio jack of a connector, call IKsJackDescription2::GetJackDescription2.
old-location: coreaudio\ksjack_description2.htm
old-project: CoreAudio
ms.assetid: 67714767-24b8-4838-953a-d6aca0c55bbb
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*PKSJACK_DESCRIPTION2, KSJACK_DESCRIPTION2, KSJACK_DESCRIPTION2 structure [Core Audio], PKSJACK_DESCRIPTION2, PKSJACK_DESCRIPTION2 structure pointer [Core Audio], _tagKSJACK_DESCRIPTION2, coreaudio.ksjack_description2, devicetopology/KSJACK_DESCRIPTION2, devicetopology/PKSJACK_DESCRIPTION2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: devicetopology.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: KSJACK_DESCRIPTION2, *PKSJACK_DESCRIPTION2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - KSJACK_DESCRIPTION2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _tagKSJACK_DESCRIPTION2 structure


## -description



The <b>KSJACK_DESCRIPTION2</b> structure describes an audio jack.

To get the description of an audio jack of a connector, call <a href="https://msdn.microsoft.com/724a75c2-22be-431c-b29a-8bf916d085e7">IKsJackDescription2::GetJackDescription2</a>.




## -struct-fields




### -field DeviceStateInfo

Reserved for future use.


### -field JackCapabilities

Stores the audio jack's capabilities: jack presence detection capability 
                                       or dynamic format changing capability. The constants that can be stored in this member of the structure are defined in Ksmedia.h as follows:

<ul>
<li>JACKDESC2_PRESENCE_DETECT_CAPABILITY       (0x00000001)</li>
<li>JACKDESC2_DYNAMIC_FORMAT_CHANGE_CAPABILITY (0x00000002)
</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/9a3d7631-6892-457a-91ab-484ae867fd9f">IKsJackDescription2</a>
 

 

