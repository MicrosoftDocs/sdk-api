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

# MfCard_Des_s structure


## -description


The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by <i>one</i> of the hardware functions provided by an instance of a multifunction device. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field PMF_Count

Must be 1.


### -field PMF_Type

<i>Not used.</i>


### -field PMF_Flags

One bit flag is defined, as described in the following table.

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
fPMF_AUDIO_ENABLE

</td>
<td>
If set, audio is enabled.

</td>
</tr>
</table>
 


### -field PMF_ConfigOptions

Contents of the 8-bit PCMCIA Configuration Option Register.


### -field PMF_IoResourceIndex

Zero-based index indicating the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548201">IO_RESOURCE</a> structure that describes the I/O resources for the hardware function being described by this MFCARD_DES structure.


### -field PMF_Reserved

<i>Not used.</i>


### -field PMF_ConfigRegisterBase

Offset from the beginning of the card's attribute memory space to the base configuration register address.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548201">IO_RESOURCE</a>
 

 

