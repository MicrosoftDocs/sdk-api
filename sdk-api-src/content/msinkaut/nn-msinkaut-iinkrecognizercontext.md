---
UID: NN:msinkaut.IInkRecognizerContext
title: IInkRecognizerContext
author: windows-sdk-content
description: "."
old-location: tablet\iinkrecognizercontext.htm
tech.root: tablet
ms.assetid: D3DC08E9-19CC-4281-9C71-CB9B8CBDDB7F
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IInkRecognizerContext, IInkRecognizerContext interface [Tablet PC], IInkRecognizerContext interface [Tablet PC],described, msinkaut/IInkRecognizerContext, tablet.iinkrecognizercontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msinkaut.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkRecognizerContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizerContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRecognizerContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizerContext</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cc319af-cd0b-4089-928b-cae6c86f6f61">Recognition</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> has generated results from the <a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a> method.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e86a4d5-c0a7-4283-81cc-ec3a26f74880">RecognitionWithAlternates</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a> has generated results after calling the <a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates Method</a> method.
        

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkRecognizerContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a>
</td>
<td align="left" width="63%">
Causes the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="https://msdn.microsoft.com/0cc319af-cd0b-4089-928b-cae6c86f6f61">Recognition</a> event when recognition is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates</a>
</td>
<td align="left" width="63%">
Causes the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="https://msdn.microsoft.com/5e86a4d5-c0a7-4283-81cc-ec3a26f74880">RecognitionWithAlternates</a> event when recognition is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f376e177-7714-4771-8aa4-13f91a26395a">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a384edf8-3b3d-4e0c-b39c-976798457076">EndInkInput</a>
</td>
<td align="left" width="63%">

<a href="https://msdn.microsoft.com/a384edf8-3b3d-4e0c-b39c-976798457076">EndInkInput</a> is no longer available for use for recognizers of western languages as of Windows Vista.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5344044a-0973-4ab2-bf5c-74e0d07d4e76">IsStringSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the system dictionary, user dictionary, or <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">word list</a> contain a specified string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83695dfd-3634-47e7-8311-7216876a827a">Recognize</a>
</td>
<td align="left" width="63%">
Performs recognition on an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection and returns recognition results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ece9a1-cbc3-43ae-85ec-e3bf78a4e5a0">StopBackgroundRecognition</a>
</td>
<td align="left" width="63%">
Ends background recognition that was started with a call to <a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a> or <a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizerContext</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8cb3e41f-803f-4f88-81bb-b2222c070610">CharacterAutoCompletion</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the character Autocomplete mode, which determines when characters or words are recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/11a76706-e2e5-4ae5-bdc2-5354514ea29f">Factoid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/706d28c3-fc5d-496a-a957-daf5ba8d47ca">Guide</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide</a> to use for ink input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97">PrefixText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the characters that come before the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection in the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a15234b1-1ac2-4241-b1cd-eb9702ee2a49">Recognizer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object used by the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/af31559b-741e-4af2-8c35-9e34ad1af85f">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection associated with the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f7fb1314-b5d5-4aa9-91d0-cbd649aded39">SuffixText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the characters that come after the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection in the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/893950d4-c19c-4635-ad66-6e363860280a">WordList</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the word list that is used in the recognition process to improve the recognition results.

</td>
</tr>
</table> 

