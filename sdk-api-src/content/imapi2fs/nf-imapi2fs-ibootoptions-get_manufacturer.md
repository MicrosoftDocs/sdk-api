---
UID: NF:imapi2fs.IBootOptions.get_Manufacturer
title: IBootOptions::get_Manufacturer (imapi2fs.h)
author: windows-sdk-content
description: Retrieves the identifier of the manufacturer of the CD.
old-location: imapi\ibootoptions_get_manufacturer.htm
tech.root: imapi
ms.assetid: e9c75760-42e8-4ad0-aa5c-82bfdc1327af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBootOptions interface [IMAPI],get_Manufacturer method, IBootOptions.get_Manufacturer, IBootOptions::get_Manufacturer, get_Manufacturer, get_Manufacturer method [IMAPI], get_Manufacturer method [IMAPI],IBootOptions interface, imapi.ibootoptions_get_manufacturer, imapi2fs/IBootOptions::get_Manufacturer
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
 - IBootOptions.get_Manufacturer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBootOptions::get_Manufacturer


## -description


Retrieves the identifier of the manufacturer of the CD.


## -parameters




### -param pVal [out]

Identifier of the manufacturer of the CD.


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



<a href="https://msdn.microsoft.com/485b36f0-6c33-48da-8ac5-64f4fc13fd68">IBootOptions::put_Manufacturer</a>
 

 

