---
UID: NF:imapi2fs.IBootOptions.get_Emulation
title: IBootOptions::get_Emulation
author: windows-sdk-content
description: Retrieves the media type that the boot image is intended to emulate.
old-location: imapi\ibootoptions_get_emulation.htm
tech.root: imapi
ms.assetid: ade69c2b-ff25-4993-bf4c-ee372e3cc1b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBootOptions interface [IMAPI],get_Emulation method, IBootOptions.get_Emulation, IBootOptions::get_Emulation, get_Emulation, get_Emulation method [IMAPI], get_Emulation method [IMAPI],IBootOptions interface, imapi.ibootoptions_get_emulation, imapi2fs/IBootOptions::get_Emulation
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
 - IBootOptions.get_Emulation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBootOptions::get_Emulation


## -description


Retrieves the media type that the boot image is intended to emulate.


## -parameters




### -param pVal [out]

Media type that the boot image is intended to emulate. For possible values, see the <a href="https://msdn.microsoft.com/53e87d6d-9547-4437-9548-652cfcbd308e">EmulationType</a> enumeration type. 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/93ed301e-fdea-451c-9ab0-6ea9a7fd45de">IBootOptions::put_Emulation</a>
 

 

