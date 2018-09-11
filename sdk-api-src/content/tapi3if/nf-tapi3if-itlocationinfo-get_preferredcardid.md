---
UID: NF:tapi3if.ITLocationInfo.get_PreferredCardID
title: ITLocationInfo::get_PreferredCardID
author: windows-sdk-content
description: The get_PreferredCardID method gets the preferred calling card identifier for dialing from the current location.
old-location: tapi3\itlocationinfo_get_preferredcardid.htm
tech.root: tapi
ms.assetid: 7881a005-1bab-47a1-a657-31584d3f2713
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_PreferredCardID method, ITLocationInfo.get_PreferredCardID, ITLocationInfo::get_PreferredCardID, _tapi3_itlocationinfo_get_preferredcardid, get_PreferredCardID, get_PreferredCardID method [TAPI 2.2], get_PreferredCardID method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_preferredcardid, tapi3if/ITLocationInfo::get_PreferredCardID
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
 - ITLocationInfo.get_PreferredCardID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLocationInfo::get_PreferredCardID


## -description


The 
<b>get_PreferredCardID</b> method gets the preferred calling card identifier for dialing from the current location.


## -parameters




### -param plCardID [out]

Calling card ID.


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
The <i>plCardID</i> parameter is not a valid pointer.

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



The value that this method returns corresponds to the <b>dwPreferredCardID</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

