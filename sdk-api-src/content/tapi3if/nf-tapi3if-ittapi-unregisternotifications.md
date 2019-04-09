---
UID: NF:tapi3if.ITTAPI.UnregisterNotifications
title: ITTAPI::UnregisterNotifications (tapi3if.h)
author: windows-sdk-content
description: The UnregisterNotifications method removes any incoming call notification registrations that have been performed using ITTAPI::RegisterCallNotifications.
old-location: tapi3\ittapi_unregisternotifications.htm
tech.root: Tapi
ms.assetid: 66717165-1c29-4d77-b6ac-8c3638fb11f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],UnregisterNotifications method, ITTAPI.UnregisterNotifications, ITTAPI::UnregisterNotifications, UnregisterNotifications, UnregisterNotifications method [TAPI 2.2], UnregisterNotifications method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_unregisternotifications, tapi3.ittapi_unregisternotifications, tapi3if/ITTAPI::UnregisterNotifications
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
 - ITTAPI.UnregisterNotifications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI::UnregisterNotifications


## -description


The 
<b>UnregisterNotifications</b> method removes any incoming call notification registrations that have been performed using 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>.


## -parameters




### -param lRegister [in]

The value returned by the 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">RegisterCallNotifications</a> method in the <i>plRegister</i> parameter.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not yet been initialized or the <i>lRegister</i> parameter is not valid.

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
 




## -see-also




<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

