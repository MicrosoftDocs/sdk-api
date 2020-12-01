---
UID: NF:tapi3if.ITTAPI.SetApplicationPriority
title: ITTAPI::SetApplicationPriority (tapi3if.h)
description: The SetApplicationPriority method allows an application to set its priority in the handoff priority list for a particular media type or Assisted Telephony request mode, or to remove itself from the priority list.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","SetApplicationPriority method","ITTAPI.SetApplicationPriority","ITTAPI::SetApplicationPriority","SetApplicationPriority","SetApplicationPriority method [TAPI 2.2]","SetApplicationPriority method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_setapplicationpriority","tapi3.ittapi_setapplicationpriority","tapi3if/ITTAPI::SetApplicationPriority"]
old-location: tapi3\ittapi_setapplicationpriority.htm
tech.root: tapi3
ms.assetid: ca049695-02d0-4b30-ad1f-60cdbf0a4dbd
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],SetApplicationPriority method, ITTAPI.SetApplicationPriority, ITTAPI::SetApplicationPriority, SetApplicationPriority, SetApplicationPriority method [TAPI 2.2], SetApplicationPriority method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_setapplicationpriority, tapi3.ittapi_setapplicationpriority, tapi3if/ITTAPI::SetApplicationPriority
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
 - ITTAPI::SetApplicationPriority
 - tapi3if/ITTAPI::SetApplicationPriority
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
 - ITTAPI.SetApplicationPriority
---

# ITTAPI::SetApplicationPriority


## -description

The 
<b>SetApplicationPriority</b> method allows an application to set its priority in the handoff priority list for a particular media type or Assisted Telephony request mode, or to remove itself from the priority list.

## -parameters

### -param pAppFilename [in]

Pointer to <b>BSTR</b> containing name of application.

### -param lMediaType [in]

Media associated with application.

### -param fPriority [in]

The new priority for the application. If the value VARIANT_FALSE is passed, the application is removed from the priority list for the specified media or request mode (if it was already not present, no error is generated). If the value VARIANT_TRUE is passed, the application is inserted as the highest-priority application for the media or request mode (and removed from a lower-priority position, if it was already in the list).

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pAppFilename</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

The Priorities that are set with <b>SetApplicationPriority</b> will persist across reboots of the system or restarts of tapisrv. The <a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a> function opens the line with no specified call priorities. By default, the highest priority application will be the one that first called <b>ITTAPI::RegisterCallNotifications</b>.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect">ITBasicCallControl::HandoffIndirect</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>