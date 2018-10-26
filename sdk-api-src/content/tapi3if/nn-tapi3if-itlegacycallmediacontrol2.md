---
UID: NN:tapi3if.ITLegacyCallMediaControl2
title: ITLegacyCallMediaControl2
author: windows-sdk-content
description: The ITLegacyCallMediaControl2 interface is an extension of the ITLegacyCallMediaControl interface. ITLegacyCallMediaControl2 provides additional methods, primarily for tone detection and generation.
old-location: tapi3\itlegacycallmediacontrol2.htm
tech.root: TAPI
ms.assetid: 47fa5669-1c74-4c18-8370-3efe35b3573e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITLegacyCallMediaControl2, ITLegacyCallMediaControl2 interface [TAPI 2.2], ITLegacyCallMediaControl2 interface [TAPI 2.2],described, _tapi3_itlegacycallmediacontrol2, tapi3.itlegacycallmediacontrol2, tapi3if/ITLegacyCallMediaControl2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITLegacyCallMediaControl2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl2 interface


## -description


The 
<b>ITLegacyCallMediaControl2</b> interface is an extension of the 
<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a> interface. 
<b>ITLegacyCallMediaControl2</b> provides additional methods, primarily for tone detection and generation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyCallMediaControl2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITLegacyCallMediaControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyCallMediaControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/addef387-9d92-4da3-af4c-b4d40bde2e36">CreateCustomToneObject</a>
</td>
<td align="left" width="63%">
Creates a custom tone object to use with the 
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a> method. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f00391f-b63f-4fa7-82af-44584fbcd8a3">CreateDetectToneObject</a>
</td>
<td align="left" width="63%">
Creates a detect tone object to use with the 
<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">DetectTonesByCollection</a> method. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e059bfc0-3701-4e07-8c30-0a2512731080">DetectTones</a>
</td>
<td align="left" width="63%">
Enables and disables the detection of inband tones on the call. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">DetectTonesByCollection</a>
</td>
<td align="left" width="63%">
Enables and disables the detection of inband tones on the call. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff464b1e-bd4c-4807-b019-cdae6896f897">GatherDigits</a>
</td>
<td align="left" width="63%">
Initiates the gathering of digits on the specified call; extends the 
<a href="https://msdn.microsoft.com/d4dcdce0-4df5-43bb-a5ea-ea72782d5f04">ITLegacyCallMediaControl::GenerateDigits</a> method by adding a duration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcc5d3c9-a7ab-4467-a948-b9fd68afe7b4">GenerateCustomTones</a>
</td>
<td align="left" width="63%">
Generates a specified custom tone. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">GenerateCustomTonesByCollection</a>
</td>
<td align="left" width="63%">
Generates a specified custom tone. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63ea18ef-18ca-4771-a7d9-60d4e8c514a5">GenerateDigits2</a>
</td>
<td align="left" width="63%">
Causes digits to be output on the current call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c77ee53-3c40-4fdc-9a35-40a8e74b4ec4">GenerateTone</a>
</td>
<td align="left" width="63%">
Generates a specified tone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c28889f-3768-4136-ac73-80c6c5ffeac3">GetIDAsVariant</a>
</td>
<td align="left" width="63%">
Gets the identifier for the device associated with the current call

This method is intended for Visual Basic and scripting applications.  C/C++ applications should use the 
<a href="https://msdn.microsoft.com/7516f929-d782-499b-a9fb-24c44a85aa9e">ITLegacyCallMediaControl::GetID</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>
 

 

