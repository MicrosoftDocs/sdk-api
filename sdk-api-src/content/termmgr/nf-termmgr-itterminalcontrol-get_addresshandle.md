---
UID: NF:termmgr.ITTerminalControl.get_AddressHandle
title: ITTerminalControl::get_AddressHandle
author: windows-sdk-content
description: The get_AddressHandle method gets the MSP address handle.
old-location: tapi3\itterminalcontrol_get_addresshandle.htm
tech.root: TAPI
ms.assetid: 6f222dea-059a-4eda-bcbc-cd6c61cdf2fa
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITTerminalControl interface [TAPI 2.2],get_AddressHandle method, ITTerminalControl.get_AddressHandle, ITTerminalControl::get_AddressHandle, _tapi3_itterminalcontrol_get_addresshandle, get_AddressHandle, get_AddressHandle method [TAPI 2.2], get_AddressHandle method [TAPI 2.2],ITTerminalControl interface, tapi3.itterminalcontrol_get_addresshandle, termmgr/ITTerminalControl::get_AddressHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: termmgr.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalControl.get_AddressHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalControl::get_AddressHandle


## -description


The 
<b>get_AddressHandle</b> method gets the MSP address handle.


## -parameters




### -param phtAddress [out]

Pointer to MSP address handle.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>phtAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6fe60002-3af3-45e9-a084-7296a48e7263">ITTerminalControl</a>
 

 

