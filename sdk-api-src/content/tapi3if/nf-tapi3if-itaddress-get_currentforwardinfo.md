---
UID: NF:tapi3if.ITAddress.get_CurrentForwardInfo
title: ITAddress::get_CurrentForwardInfo
author: windows-sdk-content
description: The get_CurrentForwardInfo method gets a pointer to the current forwarding information object.
old-location: tapi3\itaddress_get_currentforwardinfo.htm
tech.root: tapi
ms.assetid: 7817ac03-d9fc-4042-ae7d-350ee6cbef53
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_CurrentForwardInfo method, ITAddress.get_CurrentForwardInfo, ITAddress::get_CurrentForwardInfo, _tapi3_itaddress_get_currentforwardinfo, get_CurrentForwardInfo, get_CurrentForwardInfo method [TAPI 2.2], get_CurrentForwardInfo method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_currentforwardinfo, tapi3if/ITAddress::get_CurrentForwardInfo
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
 - ITAddress.get_CurrentForwardInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress::get_CurrentForwardInfo


## -description


The 
<b>get_CurrentForwardInfo</b> method gets a pointer to the current forwarding information object.


## -parameters




### -param ppForwardInfo [out]

Pointer to 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> interface.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

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
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_INVALPOINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppForwardInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> interface returned by <b>ITAddress::get_ForwardInfo</b>. The application must call <b>Release</b> on the 
<b>ITForwardInformation</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>
 

 

