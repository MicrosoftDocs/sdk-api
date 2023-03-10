---
UID: NF:tapi3if.ITLegacyAddressMediaControl.SetDevConfig
title: ITLegacyAddressMediaControl::SetDevConfig (tapi3if.h)
description: The SetDevConfig function allows the application to restore the configuration of a media stream device on a line device to a setup previously obtained using GetDevConfig.
helpviewer_keywords: ["ITLegacyAddressMediaControl interface [TAPI 2.2]","SetDevConfig method","ITLegacyAddressMediaControl.SetDevConfig","ITLegacyAddressMediaControl::SetDevConfig","SetDevConfig","SetDevConfig method [TAPI 2.2]","SetDevConfig method [TAPI 2.2]","ITLegacyAddressMediaControl interface","_tapi3_itlegacyaddressmediacontrol_setdevconfig","tapi3.itlegacyaddressmediacontrol_setdevconfig","tapi3if/ITLegacyAddressMediaControl::SetDevConfig"]
old-location: tapi3\itlegacyaddressmediacontrol_setdevconfig.htm
tech.root: tapi3
ms.assetid: 7c5fe0ab-8a03-41db-994b-9786782cf7c1
ms.date: 12/05/2018
ms.keywords: ITLegacyAddressMediaControl interface [TAPI 2.2],SetDevConfig method, ITLegacyAddressMediaControl.SetDevConfig, ITLegacyAddressMediaControl::SetDevConfig, SetDevConfig, SetDevConfig method [TAPI 2.2], SetDevConfig method [TAPI 2.2],ITLegacyAddressMediaControl interface, _tapi3_itlegacyaddressmediacontrol_setdevconfig, tapi3.itlegacyaddressmediacontrol_setdevconfig, tapi3if/ITLegacyAddressMediaControl::SetDevConfig
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
 - ITLegacyAddressMediaControl::SetDevConfig
 - tapi3if/ITLegacyAddressMediaControl::SetDevConfig
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
 - ITLegacyAddressMediaControl.SetDevConfig
---

# ITLegacyAddressMediaControl::SetDevConfig


## -description

The 
<b>SetDevConfig</b> function allows the application to restore the configuration of a media stream device on a line device to a setup previously obtained using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getdevconfig">GetDevConfig</a>.

## -parameters

### -param pDeviceClass [in]

Pointer to <b>BSTR</b> containing 
<a href="/windows/desktop/Tapi/tapi-device-classes">TAPI device class</a> for which configuration information is needed.

### -param dwSize [in]

Size of configuration array.

### -param pDeviceConfig [in]

Pointer to the array of bytes containing device configuration information obtained by a call to 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getdevconfig">GetDevConfig</a>.

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
The <i>pDeviceClass</i>, <i>pdwSize</i>, or <i>ppDeviceConfig</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> parameter is zero.

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

This method is a COM wrapper for the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a> TAPI 2.1 function.

The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getid">GetID</a> must be performed prior to calling this method.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDeviceClass</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

<b>TAPI 2.1 Cross-References:  </b><a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>, <a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a>

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getdevconfig">GetDevConfig</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>