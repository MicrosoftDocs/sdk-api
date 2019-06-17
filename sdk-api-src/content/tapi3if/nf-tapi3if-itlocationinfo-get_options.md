---
UID: NF:tapi3if.ITLocationInfo.get_Options
title: ITLocationInfo::get_Options (tapi3if.h)
author: windows-sdk-content
description: The get_Options method gets an indicator of whether the current location supports pulse or tone dialing.
old-location: tapi3\itlocationinfo_get_options.htm
tech.root: Tapi
ms.assetid: a53d7029-25a0-460c-97dd-c49355cc2ddc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_Options method, ITLocationInfo.get_Options, ITLocationInfo::get_Options, _tapi3_itlocationinfo_get_options, get_Options, get_Options method [TAPI 2.2], get_Options method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_options, tapi3if/ITLocationInfo::get_Options
ms.topic: method
f1_keywords: ["tapi3if/ITLocationInfo.get_Options"]
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
ms.custom: 19H1
---

# ITLocationInfo::get_Options


## -description


The 
<b>get_Options</b> method gets an indicator of whether the current location supports pulse or tone dialing.


## -parameters




### -param plOptions [out]

Dialing options, as indicated by values from 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linelocationoption--constants">LINELOCATIONOPTION_ Constants</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linelocationentry_tag">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linelocationentry_tag">LINELOCATIONENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>
 

 

