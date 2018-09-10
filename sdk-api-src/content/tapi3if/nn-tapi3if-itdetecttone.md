---
UID: NN:tapi3if.ITDetectTone
title: ITDetectTone
author: windows-sdk-content
description: The ITDetectTone interface exposes methods that allow an application to specify the tones and tone characteristics that should cause the TAPI Server to generate a tone event.
old-location: tapi3\itdetecttone.htm
tech.root: tapi
ms.assetid: c03db3e2-3dc9-443f-8acf-66c06940e0b9
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITDetectTone, ITDetectTone interface [TAPI 2.2], ITDetectTone interface [TAPI 2.2],described, _tapi3_itdetecttone, tapi3.itdetecttone, tapi3if/ITDetectTone
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
 - ITDetectTone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDetectTone interface


## -description


The 
<b>ITDetectTone</b> interface exposes methods that allow an application to specify the tones and tone characteristics that should cause the TAPI Server to generate a tone event. The 
<a href="https://msdn.microsoft.com/3f00391f-b63f-4fa7-82af-44584fbcd8a3">ITLegacyCallMediaControl2::CreateDetectToneObject</a> and 
<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">ITLegacyCallMediaControl2::DetectTonesByCollection</a> methods create the 
<b>ITDetectTone</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDetectTone</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITDetectTone</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a3ffba50-664d-42d2-87b2-fe6943715e85">get_AppSpecific</a>
</td>
<td align="left" width="63%">
Gets the application-defined tag that identifies the tone to detect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c1f8900-1384-4fb5-8931-90bb0d100d41">get_Duration</a>
</td>
<td align="left" width="63%">
Gets the length of time during which a tone should be present before the TAPI Server generates a tone event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7137eba-c863-4125-9602-14bfba814b2a">get_Frequency</a>
</td>
<td align="left" width="63%">
Gets the frequency of the tone for which the TAPI Server generates a tone event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d008cda-bb01-4249-a0ca-a40d2daacbc4">put_AppSpecific</a>
</td>
<td align="left" width="63%">
Sets the application-defined tag that identifies the tone to detect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a64181ca-e8d6-48fc-89ef-b91268b709aa">put_Duration</a>
</td>
<td align="left" width="63%">
Sets the length of time during which a tone should be present before the TAPI Server generates a tone event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83895e55-61ab-464b-bb85-e81d15dd96e1">put_Frequency</a>
</td>
<td align="left" width="63%">
Sets the frequency of the tone for which the TAPI Server generates a tone event.

</td>
</tr>
</table> 

