---
UID: NF:tapi3if.ITCallInfo.get_Privilege
title: ITCallInfo::get_Privilege
author: windows-sdk-content
description: The get_Privilege method gets the call privilege of the application for the current call, such as CP_MONITOR.
old-location: tapi3\itcallinfo_get_privilege.htm
tech.root: Tapi
ms.assetid: 64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_Privilege method, ITCallInfo.get_Privilege, ITCallInfo::get_Privilege, _tapi3_itcallinfo_get_privilege, get_Privilege, get_Privilege method [TAPI 2.2], get_Privilege method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_privilege, tapi3if/ITCallInfo::get_Privilege
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
 - ITCallInfo.get_Privilege
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfo::get_Privilege


## -description


The 
<b>get_Privilege</b> method gets the 
<a href="https://msdn.microsoft.com/8d2ab3d2-9531-40fc-910d-2bd81a075cc3">call privilege</a> of the application for the current call, such as CP_MONITOR.


## -parameters




### -param pPrivilege [out]

Pointer to 
<a href="https://msdn.microsoft.com/8d2ab3d2-9531-40fc-910d-2bd81a075cc3">CALL_PRIVILEGE</a>.


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
The <i>pPrivilege</i> parameter is not a valid pointer.

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



<b>TAPI 2.1 Cross-Reference: </b><a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>





## -see-also




<a href="https://msdn.microsoft.com/8d2ab3d2-9531-40fc-910d-2bd81a075cc3">CALL_PRIVILEGE</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

