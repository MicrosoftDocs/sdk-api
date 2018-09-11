---
UID: NF:tapi3if.ITLegacyCallMediaControl2.DetectTonesByCollection
title: ITLegacyCallMediaControl2::DetectTonesByCollection
author: windows-sdk-content
description: The DetectTonesByCollection method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.
old-location: tapi3\itlegacycallmediacontrol2_detecttonesbycollection.htm
tech.root: tapi
ms.assetid: 09cbcd9d-66cd-4131-b45c-cb3898d8446d
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: DetectTonesByCollection, DetectTonesByCollection method [TAPI 2.2], DetectTonesByCollection method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],DetectTonesByCollection method, ITLegacyCallMediaControl2.DetectTonesByCollection, ITLegacyCallMediaControl2::DetectTonesByCollection, _tapi3_itlegacycallmediacontrol2_detecttonesbycollection, tapi3.itlegacycallmediacontrol2_detecttonesbycollection, tapi3if/ITLegacyCallMediaControl2::DetectTonesByCollection
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
 - ITLegacyCallMediaControl2.DetectTonesByCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2::DetectTonesByCollection


## -description


The 
<b>DetectTonesByCollection</b> method enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="https://msdn.microsoft.com/e059bfc0-3701-4e07-8c30-0a2512731080">DetectTones</a> method instead.


## -parameters




### -param pDetectToneCollection [in]

Pointer to an 
<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a> interface containing a collection of 
<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a> interface pointers that represent the tones to monitor. Each tone in the list has an application-defined tag field that is used to identify the individual tones when tone detection is reported by a <b>TE_TONEEVENT</b> event. For more information, see the following Remarks section.


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
The <i>pDetectToneCollection</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the tones buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call must be in the <i>connected</i> state.

</td>
</tr>
</table>
 




## -remarks



This method translates to a TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/47fe21f2-7896-4ccf-8c26-33430b2081ac">lineMonitorTones</a> call.

To cancel tone monitoring in progress, call the 
<b>DetectTonesByCollection</b> method and specify an empty collection. To change the list of tones to monitor, call this method and specify a new tone collection.




## -see-also




<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a>



<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a>



<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

