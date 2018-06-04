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

# IBootOptions::put_Emulation


## -description


Sets the media type that the boot image is intended to emulate.


## -parameters




### -param newVal [in]

Media type that the boot image is intended to emulate. For possible values, see the <a href="https://msdn.microsoft.com/53e87d6d-9547-4437-9548-652cfcbd308e">EmulationType</a> enumeration type. The default value is <b>EmulationNone</b>, which means the BIOS will not emulate any device type or special sector size for the CD during boot from the CD.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The emulation type requested does not match the boot image size.

Value: 0xC0AAB14A

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/ade69c2b-ff25-4993-bf4c-ee372e3cc1b0">IBootOptions::get_Emulation</a>
 

 

