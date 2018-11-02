---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GetIDAsVariant
title: ITLegacyCallMediaControl2::GetIDAsVariant
author: windows-sdk-content
description: The GetIDAsVariant method gets the identifier for the device associated with the current call.
old-location: tapi3\itlegacycallmediacontrol2_getidasvariant.htm
tech.root: tapi
ms.assetid: 6c28889f-3768-4136-ac73-80c6c5ffeac3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetIDAsVariant, GetIDAsVariant method [TAPI 2.2], GetIDAsVariant method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GetIDAsVariant method, ITLegacyCallMediaControl2.GetIDAsVariant, ITLegacyCallMediaControl2::GetIDAsVariant, _tapi3_itlegacycallmediacontrol2_getidasvariant, tapi3.itlegacycallmediacontrol2_getidasvariant, tapi3if/ITLegacyCallMediaControl2::GetIDAsVariant
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2::GetIDAsVariant


## -description


The 
<b>GetIDAsVariant</b> method gets the identifier for the device associated with the current call.

This method is intended for Visual Basic and scripting applications.  C/C++ applications should use the 
<a href="https://msdn.microsoft.com/7516f929-d782-499b-a9fb-24c44a85aa9e">ITLegacyCallMediaControl::GetID</a> method.


## -parameters




### -param bstrDeviceClass [in]

<b>BSTR</b> representing the 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI device class</a>.


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




<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>



<a href="https://msdn.microsoft.com/7516f929-d782-499b-a9fb-24c44a85aa9e">ITLegacyCallMediaControl::GetID</a>
 

 

