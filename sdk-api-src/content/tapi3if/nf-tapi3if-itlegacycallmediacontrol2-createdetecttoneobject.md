---
UID: NF:tapi3if.ITLegacyCallMediaControl2.CreateDetectToneObject
title: ITLegacyCallMediaControl2::CreateDetectToneObject
author: windows-sdk-content
description: The CreateDetectToneObject method creates a detect tone object to use with the DetectTonesByCollection method.
old-location: tapi3\itlegacycallmediacontrol2_createdetecttoneobject.htm
tech.root: tapi
ms.assetid: 3f00391f-b63f-4fa7-82af-44584fbcd8a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDetectToneObject, CreateDetectToneObject method [TAPI 2.2], CreateDetectToneObject method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],CreateDetectToneObject method, ITLegacyCallMediaControl2.CreateDetectToneObject, ITLegacyCallMediaControl2::CreateDetectToneObject, _tapi3_itlegacycallmediacontrol2_createdetecttoneobject, tapi3.itlegacycallmediacontrol2_createdetecttoneobject, tapi3if/ITLegacyCallMediaControl2::CreateDetectToneObject
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
 - ITLegacyCallMediaControl2.CreateDetectToneObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2::CreateDetectToneObject


## -description


The 
<b>CreateDetectToneObject</b> method creates a detect tone object to use with the 
<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">DetectTonesByCollection</a> method.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="https://msdn.microsoft.com/e059bfc0-3701-4e07-8c30-0a2512731080">DetectTones</a> method instead.


## -parameters




### -param ppDetectTone [out]

Pointer to an 
<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ppDetectTone</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the object.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a> interface returned by <b>ITLegacyCallMediaControl2::CreateDetectToneObject</b>. The application must call the <b>Release</b> method on the 
<b>ITDetectTone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">DetectTonesByCollection</a>



<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a>



<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

