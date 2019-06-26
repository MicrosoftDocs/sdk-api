---
UID: NN:tapi3if.ITLegacyCallMediaControl
title: ITLegacyCallMediaControl (tapi3if.h)
author: windows-sdk-content
description: The ITLegacyCallMediaControl interface supports legacy applications that must communicate directly with a device. This interface is exposed on the Call Object and can be created by calling QueryInterface on ITBasicCallControl.
old-location: tapi3\itlegacycallmediacontrol.htm
tech.root: Tapi
ms.assetid: 73288c46-6c6d-4938-9bb7-4d94acfc67f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITLegacyCallMediaControl, ITLegacyCallMediaControl interface [TAPI 2.2], ITLegacyCallMediaControl interface [TAPI 2.2],described, _tapi3_itlegacycallmediacontrol, tapi3.itlegacycallmediacontrol, tapi3if/ITLegacyCallMediaControl
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITLegacyCallMediaControl"
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
 - ITLegacyCallMediaControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyCallMediaControl interface


## -description


The 
<b>ITLegacyCallMediaControl</b> interface supports legacy applications that must communicate directly with a device. This interface is exposed on the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a> and can be created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a> interface is an extension of the 
<b>ITLegacyCallMediaControl</b> interface. 
<b>ITLegacyCallMediaControl2</b> provides additional methods, primarily for tone detection and generation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyCallMediaControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITLegacyCallMediaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyCallMediaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-detectdigits">DetectDigits</a>
</td>
<td align="left" width="63%">
Sets 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-digitmode--constants">mode</a> for digit detection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-generatedigits">GenerateDigits</a>
</td>
<td align="left" width="63%">
Sends digits to call destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-getid">GetID</a>
</td>
<td align="left" width="63%">
Gets identifier for device associated with the current call. This method is intended for Visual Basic and scripting applications.

This method is intended for C/C++ applications.  Visual Basic and scripting applications should use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-getidasvariant">ITLegacyCallMediaControl2::GetIDAsVariant</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-monitormedia">MonitorMedia</a>
</td>
<td align="left" width="63%">
Sets monitoring for a given media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-setmediatype">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media type</a> for call.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>
 

 

