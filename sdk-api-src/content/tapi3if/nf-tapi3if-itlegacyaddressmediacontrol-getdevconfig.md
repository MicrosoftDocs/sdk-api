---
UID: NF:tapi3if.ITLegacyAddressMediaControl.GetDevConfig
title: ITLegacyAddressMediaControl::GetDevConfig (tapi3if.h)
description: The GetDevConfig method returns an opaque data structure.
helpviewer_keywords: ["GetDevConfig","GetDevConfig method [TAPI 2.2]","GetDevConfig method [TAPI 2.2]","ITLegacyAddressMediaControl interface","ITLegacyAddressMediaControl interface [TAPI 2.2]","GetDevConfig method","ITLegacyAddressMediaControl.GetDevConfig","ITLegacyAddressMediaControl::GetDevConfig","_tapi3_itlegacyaddressmediacontrol_getdevconfig","tapi3.itlegacyaddressmediacontrol_getdevconfig","tapi3if/ITLegacyAddressMediaControl::GetDevConfig"]
old-location: tapi3\itlegacyaddressmediacontrol_getdevconfig.htm
tech.root: tapi3
ms.assetid: ed8cc556-31a5-4725-92fe-1f78c16aadcd
ms.date: 12/05/2018
ms.keywords: GetDevConfig, GetDevConfig method [TAPI 2.2], GetDevConfig method [TAPI 2.2],ITLegacyAddressMediaControl interface, ITLegacyAddressMediaControl interface [TAPI 2.2],GetDevConfig method, ITLegacyAddressMediaControl.GetDevConfig, ITLegacyAddressMediaControl::GetDevConfig, _tapi3_itlegacyaddressmediacontrol_getdevconfig, tapi3.itlegacyaddressmediacontrol_getdevconfig, tapi3if/ITLegacyAddressMediaControl::GetDevConfig
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
 - ITLegacyAddressMediaControl::GetDevConfig
 - tapi3if/ITLegacyAddressMediaControl::GetDevConfig
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
 - ITLegacyAddressMediaControl.GetDevConfig
---

# ITLegacyAddressMediaControl::GetDevConfig


## -description

The 
<b>GetDevConfig</b> method returns an opaque data structure. The exact contents are specific to the service provider and device class. The data structure specifies the configuration of a device associated with a particular line device. For example, the contents of this structure could specify data rate, character format, modulation schemes, and error control protocol settings for a datamodem device associated with the line.

## -parameters

### -param pDeviceClass [in]

Pointer to <b>BSTR</b> containing 
<a href="/windows/desktop/Tapi/tapi-device-classes">TAPI device class</a> for which configuration information is needed.

### -param pdwSize [out]

Pointer to size of configuration array.

### -param ppDeviceConfig [out]

Pointer to array of bytes containing device configuration information.

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
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">LineGetDevConfig</a> TAPI 2.1 function.

The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getid">GetID</a> must be performed prior to calling this method.

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDeviceClass</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

The application must call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory allocated for the <i>ppDeviceConfig</i> parameter.

<b>TAPI 2.1 Cross-References:  </b><a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>, <a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-setdevconfig">SetDevConfig</a>