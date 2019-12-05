---
UID: NN:tapi3if.ITLegacyCallMediaControl2
title: ITLegacyCallMediaControl2 (tapi3if.h)
description: The ITLegacyCallMediaControl2 interface is an extension of the ITLegacyCallMediaControl interface. ITLegacyCallMediaControl2 provides additional methods, primarily for tone detection and generation.
old-location: tapi3\itlegacycallmediacontrol2.htm
tech.root: Tapi
ms.assetid: 47fa5669-1c74-4c18-8370-3efe35b3573e
ms.date: 12/05/2018
ms.keywords: ITLegacyCallMediaControl2, ITLegacyCallMediaControl2 interface [TAPI 2.2], ITLegacyCallMediaControl2 interface [TAPI 2.2],described, _tapi3_itlegacycallmediacontrol2, tapi3.itlegacycallmediacontrol2, tapi3if/ITLegacyCallMediaControl2
ms.topic: interface
f1_keywords:
- tapi3if/ITLegacyCallMediaControl2
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyCallMediaControl2 interface


## -description


The 
<b>ITLegacyCallMediaControl2</b> interface is an extension of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a> interface. 
<b>ITLegacyCallMediaControl2</b> provides additional methods, primarily for tone detection and generation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyCallMediaControl2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITLegacyCallMediaControl2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-createcustomtoneobject">CreateCustomToneObject</a>
</td>
<td align="left" width="63%">
Creates a custom tone object to use with the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">GenerateCustomTonesByCollection</a> method. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-createdetecttoneobject">CreateDetectToneObject</a>
</td>
<td align="left" width="63%">
Creates a detect tone object to use with the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">DetectTonesByCollection</a> method. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttones">DetectTones</a>
</td>
<td align="left" width="63%">
Enables and disables the detection of inband tones on the call. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">DetectTonesByCollection</a>
</td>
<td align="left" width="63%">
Enables and disables the detection of inband tones on the call. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-gatherdigits">GatherDigits</a>
</td>
<td align="left" width="63%">
Initiates the gathering of digits on the specified call; extends the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-generatedigits">ITLegacyCallMediaControl::GenerateDigits</a> method by adding a duration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtones">GenerateCustomTones</a>
</td>
<td align="left" width="63%">
Generates a specified custom tone. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">GenerateCustomTonesByCollection</a>
</td>
<td align="left" width="63%">
Generates a specified custom tone. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatedigits2">GenerateDigits2</a>
</td>
<td align="left" width="63%">
Causes digits to be output on the current call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatetone">GenerateTone</a>
</td>
<td align="left" width="63%">
Generates a specified tone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-getidasvariant">GetIDAsVariant</a>
</td>
<td align="left" width="63%">
Gets the identifier for the device associated with the current call

This method is intended for Visual Basic and scripting applications.  C/C++ applications should use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-getid">ITLegacyCallMediaControl::GetID</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>
 

 

