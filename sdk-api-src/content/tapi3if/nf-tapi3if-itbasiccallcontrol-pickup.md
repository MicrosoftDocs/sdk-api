---
UID: NF:tapi3if.ITBasicCallControl.Pickup
title: ITBasicCallControl::Pickup
author: windows-sdk-content
description: The Pickup method picks up a call alerting at the specified group identification.
old-location: tapi3\itbasiccallcontrol_pickup.htm
old-project: tapi
ms.assetid: 25da3cf2-50f0-4f64-94ce-cf952e057376
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],Pickup method, ITBasicCallControl.Pickup, ITBasicCallControl::Pickup, Pickup, Pickup method [TAPI 2.2], Pickup method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_pickup, tapi3.itbasiccallcontrol_pickup, tapi3if/ITBasicCallControl::Pickup
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
 - ITBasicCallControl.Pickup
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl::Pickup


## -description


The 
Pickup method picks up a call alerting at the specified group identification.


## -parameters




### -param pGroupID [in]

Pointer to a <b>BSTR</b> containing the group identifier to which the alerting station belongs.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Pickup did not succeed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pGroupID</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="https://msdn.microsoft.com/library/ms221458(v=VS.85).aspx">SysAllocString</a> to allocate memory for the <i>pGroupID</i> parameter and use 
<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a">Pickup overview</a>



<a href="https://msdn.microsoft.com/94773ca0-8ea4-443f-9c61-81969dd72a7a">linePickup</a>
 

 

