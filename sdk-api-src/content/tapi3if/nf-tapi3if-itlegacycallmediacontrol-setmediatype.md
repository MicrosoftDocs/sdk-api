---
UID: NF:tapi3if.ITLegacyCallMediaControl.SetMediaType
title: ITLegacyCallMediaControl::SetMediaType
author: windows-sdk-content
description: The SetMediaType method sets the media type(s) for the current call in its LINECALLINFO structure. For more information, see lineSetMediaMode.
old-location: tapi3\itlegacycallmediacontrol_setmediatype.htm
tech.root: tapi
ms.assetid: 627fe465-40f6-481e-9fd6-3fc3e2931e18
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITLegacyCallMediaControl interface [TAPI 2.2],SetMediaType method, ITLegacyCallMediaControl.SetMediaType, ITLegacyCallMediaControl::SetMediaType, SetMediaType, SetMediaType method [TAPI 2.2], SetMediaType method [TAPI 2.2],ITLegacyCallMediaControl interface, _tapi3_itlegacycallmediacontrol_setmediatype, tapi3.itlegacycallmediacontrol_setmediatype, tapi3if/ITLegacyCallMediaControl::SetMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITLegacyCallMediaControl.SetMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl::SetMediaType


## -description


The 
<b>SetMediaType</b> method sets the media type(s) for the current call in its 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure. For more information, see 
<a href="https://msdn.microsoft.com/4a0e3fd7-9483-4d21-9b6f-bb6c04aa8226">lineSetMediaMode</a>.


## -parameters




### -param lMediaType [in]

Indicator of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.


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
The associated call object is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not valid.

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
 




## -see-also




<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>
 

 

