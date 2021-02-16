---
UID: NF:tapi3if.ITLegacyAddressMediaControl.GetID
title: ITLegacyAddressMediaControl::GetID (tapi3if.h)
description: The GetID method returns a device identifier for the specified device class associated with the current address.
helpviewer_keywords: ["GetID","GetID method [TAPI 2.2]","GetID method [TAPI 2.2]","ITLegacyAddressMediaControl interface","ITLegacyAddressMediaControl interface [TAPI 2.2]","GetID method","ITLegacyAddressMediaControl.GetID","ITLegacyAddressMediaControl::GetID","_tapi3_itlegacyaddressmediacontrol_getid","tapi3.itlegacyaddressmediacontrol_getid","tapi3if/ITLegacyAddressMediaControl::GetID"]
old-location: tapi3\itlegacyaddressmediacontrol_getid.htm
tech.root: tapi3
ms.assetid: f4fdde49-0867-4967-b975-f43bd9f6adc4
ms.date: 12/05/2018
ms.keywords: GetID, GetID method [TAPI 2.2], GetID method [TAPI 2.2],ITLegacyAddressMediaControl interface, ITLegacyAddressMediaControl interface [TAPI 2.2],GetID method, ITLegacyAddressMediaControl.GetID, ITLegacyAddressMediaControl::GetID, _tapi3_itlegacyaddressmediacontrol_getid, tapi3.itlegacyaddressmediacontrol_getid, tapi3if/ITLegacyAddressMediaControl::GetID
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
 - ITLegacyAddressMediaControl::GetID
 - tapi3if/ITLegacyAddressMediaControl::GetID
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
 - ITLegacyAddressMediaControl.GetID
---

# ITLegacyAddressMediaControl::GetID


## -description

The 
<b>GetID</b> method returns a device identifier for the specified device class associated with the current address.

This method is intended for C/C++ applications only. There is no corresponding method available for Visual Basic and scripting applications.

## -parameters

### -param pDeviceClass [in]

Pointer to <b>BSTR</b> containing 
<a href="/windows/desktop/Tapi/tapi-device-classes">TAPI device class</a> for which configuration information is needed.

### -param pdwSize [out]

Length of device identifier returned.

### -param ppDeviceID [out]

Device identifier.

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
Method failed. This may mean there is no device of a specified class associated with the current address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> or <i>ppDeviceID</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a> prior to calling this method.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDeviceClass</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

The application must call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory allocated for the <i>ppDeviceID</i> parameter.

<b>TAPI 2.1 Cross-References:  </b><a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>, <a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a>, <a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getdevconfig">GetDevConfig</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-setdevconfig">SetDevConfig</a>