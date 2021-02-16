---
UID: NF:tapi3if.ITCallInfo.get_Privilege
title: ITCallInfo::get_Privilege (tapi3if.h)
description: The get_Privilege method gets the call privilege of the application for the current call, such as CP_MONITOR.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","get_Privilege method","ITCallInfo.get_Privilege","ITCallInfo::get_Privilege","_tapi3_itcallinfo_get_privilege","get_Privilege","get_Privilege method [TAPI 2.2]","get_Privilege method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_get_privilege","tapi3if/ITCallInfo::get_Privilege"]
old-location: tapi3\itcallinfo_get_privilege.htm
tech.root: tapi3
ms.assetid: 64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_Privilege method, ITCallInfo.get_Privilege, ITCallInfo::get_Privilege, _tapi3_itcallinfo_get_privilege, get_Privilege, get_Privilege method [TAPI 2.2], get_Privilege method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_privilege, tapi3if/ITCallInfo::get_Privilege
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITCallInfo::get_Privilege
 - tapi3if/ITCallInfo::get_Privilege
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallInfo.get_Privilege
---

# ITCallInfo::get_Privilege


## -description

The 
<b>get_Privilege</b> method gets the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_privilege">call privilege</a> of the application for the current call, such as CP_MONITOR.

## -parameters

### -param pPrivilege [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_privilege">CALL_PRIVILEGE</a>.

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

<b>TAPI 2.1 Cross-Reference: </b><a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_privilege">CALL_PRIVILEGE</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>