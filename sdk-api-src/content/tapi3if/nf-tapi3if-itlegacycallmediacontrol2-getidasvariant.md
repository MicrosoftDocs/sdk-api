---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GetIDAsVariant
title: ITLegacyCallMediaControl2::GetIDAsVariant (tapi3if.h)
author: windows-sdk-content
description: The GetIDAsVariant method gets the identifier for the device associated with the current call.
old-location: tapi3\itlegacycallmediacontrol2_getidasvariant.htm
tech.root: Tapi
ms.assetid: 6c28889f-3768-4136-ac73-80c6c5ffeac3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIDAsVariant, GetIDAsVariant method [TAPI 2.2], GetIDAsVariant method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GetIDAsVariant method, ITLegacyCallMediaControl2.GetIDAsVariant, ITLegacyCallMediaControl2::GetIDAsVariant, _tapi3_itlegacycallmediacontrol2_getidasvariant, tapi3.itlegacycallmediacontrol2_getidasvariant, tapi3if/ITLegacyCallMediaControl2::GetIDAsVariant
ms.topic: method
f1_keywords: 
 - "tapi3if/ITLegacyCallMediaControl2.GetIDAsVariant"
req.header: tapi3if.h
req.include-header: 
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
 - ITLegacyCallMediaControl2.GetIDAsVariant
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyCallMediaControl2::GetIDAsVariant


## -description


The 
<b>GetIDAsVariant</b> method gets the identifier for the device associated with the current call.

This method is intended for Visual Basic and scripting applications.  C/C++ applications should use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-getid">ITLegacyCallMediaControl::GetID</a> method.


## -parameters




### -param bstrDeviceClass [in]

<b>BSTR</b> representing the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-device-classes">TAPI device class</a>.


### -param pVarDeviceID [out]

Pointer to a variant array of bytes of type VT_ARRAY | VT_UI1 which contains the identifier for the device specified in <i>bstrDeviceClass</i>.


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
The <i>pVarDeviceID</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-getid">ITLegacyCallMediaControl::GetID</a>
 

 

