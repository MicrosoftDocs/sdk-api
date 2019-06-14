---
UID: NN:tapi3if.ITDetectTone
title: ITDetectTone (tapi3if.h)
author: windows-sdk-content
description: The ITDetectTone interface exposes methods that allow an application to specify the tones and tone characteristics that should cause the TAPI Server to generate a tone event.
old-location: tapi3\itdetecttone.htm
tech.root: Tapi
ms.assetid: c03db3e2-3dc9-443f-8acf-66c06940e0b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITDetectTone, ITDetectTone interface [TAPI 2.2], ITDetectTone interface [TAPI 2.2],described, _tapi3_itdetecttone, tapi3.itdetecttone, tapi3if/ITDetectTone
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
 - ITDetectTone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDetectTone interface


## -description


The 
<b>ITDetectTone</b> interface exposes methods that allow an application to specify the tones and tone characteristics that should cause the TAPI Server to generate a tone event. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-createdetecttoneobject">ITLegacyCallMediaControl2::CreateDetectToneObject</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-detecttonesbycollection">ITLegacyCallMediaControl2::DetectTonesByCollection</a> methods create the 
<b>ITDetectTone</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDetectTone</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDetectTone</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDetectTone</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-get_appspecific">get_AppSpecific</a>
</td>
<td align="left" width="63%">
Gets the application-defined tag that identifies the tone to detect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-get_duration">get_Duration</a>
</td>
<td align="left" width="63%">
Gets the length of time during which a tone should be present before the TAPI Server generates a tone event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-get_frequency">get_Frequency</a>
</td>
<td align="left" width="63%">
Gets the frequency of the tone for which the TAPI Server generates a tone event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-put_appspecific">put_AppSpecific</a>
</td>
<td align="left" width="63%">
Sets the application-defined tag that identifies the tone to detect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-put_duration">put_Duration</a>
</td>
<td align="left" width="63%">
Sets the length of time during which a tone should be present before the TAPI Server generates a tone event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-put_frequency">put_Frequency</a>
</td>
<td align="left" width="63%">
Sets the frequency of the tone for which the TAPI Server generates a tone event.

</td>
</tr>
</table> 

