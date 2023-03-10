---
UID: NF:tapi3if.ITLegacyCallMediaControl.GetID
title: ITLegacyCallMediaControl::GetID (tapi3if.h)
description: The GetID method gets the identifier for the device associated with the current call.
helpviewer_keywords: ["GetID","GetID method [TAPI 2.2]","GetID method [TAPI 2.2]","ITLegacyCallMediaControl interface","ITLegacyCallMediaControl interface [TAPI 2.2]","GetID method","ITLegacyCallMediaControl.GetID","ITLegacyCallMediaControl::GetID","_tapi3_itlegacycallmediacontrol_getid","tapi3.itlegacycallmediacontrol_getid","tapi3if/ITLegacyCallMediaControl::GetID"]
old-location: tapi3\itlegacycallmediacontrol_getid.htm
tech.root: tapi3
ms.assetid: 7516f929-d782-499b-a9fb-24c44a85aa9e
ms.date: 12/05/2018
ms.keywords: GetID, GetID method [TAPI 2.2], GetID method [TAPI 2.2],ITLegacyCallMediaControl interface, ITLegacyCallMediaControl interface [TAPI 2.2],GetID method, ITLegacyCallMediaControl.GetID, ITLegacyCallMediaControl::GetID, _tapi3_itlegacycallmediacontrol_getid, tapi3.itlegacycallmediacontrol_getid, tapi3if/ITLegacyCallMediaControl::GetID
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
 - ITLegacyCallMediaControl::GetID
 - tapi3if/ITLegacyCallMediaControl::GetID
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
 - ITLegacyCallMediaControl.GetID
---

# ITLegacyCallMediaControl::GetID


## -description

The 
<b>GetID</b> method gets the identifier for the device associated with the current call.

This method is intended for C/C++ applications.  Visual Basic and scripting applications should use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-getidasvariant">ITLegacyCallMediaControl2::GetIDAsVariant</a> method.

## -parameters

### -param pDeviceClass [in]

Pointer to <b>BSTR</b> representing the 
<a href="/windows/desktop/Tapi/tapi-device-classes">TAPI device class</a>.

### -param pdwSize [out]

Size in bytes of device identifier.

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

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-getidasvariant">ITLegacyCallMediaControl2::GetIDAsVariant</a>