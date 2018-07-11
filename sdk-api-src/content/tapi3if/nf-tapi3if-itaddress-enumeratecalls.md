---
UID: NF:tapi3if.ITAddress.EnumerateCalls
title: ITAddress::EnumerateCalls
author: windows-sdk-content
description: The EnumerateCalls method enumerates calls on the current address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Calls method.
old-location: tapi3\itaddress_enumeratecalls.htm
old-project: tapi
ms.assetid: 2ffa90bf-3005-4fd0-b52f-b155c8b2194f
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: EnumerateCalls, EnumerateCalls method [TAPI 2.2], EnumerateCalls method [TAPI 2.2],ITAddress interface, ITAddress interface [TAPI 2.2],EnumerateCalls method, ITAddress.EnumerateCalls, ITAddress::EnumerateCalls, _tapi3_itaddress_enumeratecalls, tapi3.itaddress_enumeratecalls, tapi3if/ITAddress::EnumerateCalls
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress.EnumerateCalls
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress::EnumerateCalls


## -description


The 
<b>EnumerateCalls</b> method enumerates calls on the current address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/b0b16578-0530-4ff9-a7ce-d36527ed2da9">get_Calls</a> method.


## -parameters




### -param ppCallEnum [out]

Pointer to an 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface.


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
The <i>ppCallEnum</i> parameter is not a valid pointer.

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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface returned by <b>ITAddress::EnumerateCalls</b>. The application must call <b>Release</b> on the 
<b>IEnumCall</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/b0b16578-0530-4ff9-a7ce-d36527ed2da9">ITAddress::get_Calls</a>
 

 

