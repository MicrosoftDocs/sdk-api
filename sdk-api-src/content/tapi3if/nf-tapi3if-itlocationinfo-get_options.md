---
UID: NF:tapi3if.ITLocationInfo.get_Options
title: ITLocationInfo::get_Options
author: windows-sdk-content
description: The get_Options method gets an indicator of whether the current location supports pulse or tone dialing.
old-location: tapi3\itlocationinfo_get_options.htm
tech.root: tapi
ms.assetid: a53d7029-25a0-460c-97dd-c49355cc2ddc
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_Options method, ITLocationInfo.get_Options, ITLocationInfo::get_Options, _tapi3_itlocationinfo_get_options, get_Options, get_Options method [TAPI 2.2], get_Options method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_options, tapi3if/ITLocationInfo::get_Options
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLocationInfo.get_Options
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLocationInfo::get_Options


## -description


The 
<b>get_Options</b> method gets an indicator of whether the current location supports pulse or tone dialing.


## -parameters




### -param plOptions [out]

Dialing options, as indicated by values from 
<a href="https://msdn.microsoft.com/3b185c16-2535-4a90-855b-29e52828ea4c">LINELOCATIONOPTION_ Constants</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plOptions</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The value that this method returns corresponds to the <b>dwOptions</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

