---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

