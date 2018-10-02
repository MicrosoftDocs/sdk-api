---
UID: NF:imapi2fs.IBootOptions.put_Emulation
title: IBootOptions::put_Emulation
author: windows-sdk-content
description: Sets the media type that the boot image is intended to emulate.
old-location: imapi\ibootoptions_put_emulation.htm
tech.root: imapi
ms.assetid: 93ed301e-fdea-451c-9ab0-6ea9a7fd45de
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBootOptions interface [IMAPI],put_Emulation method, IBootOptions.put_Emulation, IBootOptions::put_Emulation, imapi.ibootoptions_put_emulation, imapi2fs/IBootOptions::put_Emulation, put_Emulation, put_Emulation method [IMAPI], put_Emulation method [IMAPI],IBootOptions interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IBootOptions.put_Emulation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

