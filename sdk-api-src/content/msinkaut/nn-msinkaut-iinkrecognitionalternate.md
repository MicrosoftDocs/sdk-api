---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInkRecognitionAlternate interface


## -description



Represents the possible word matches for segments of ink that are compared to a recognizers dictionary.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionAlternate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRecognitionAlternate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkRecognitionAlternate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c199960-e0ee-4370-a302-a45a3dbe8b28">AlternatesWithConstantPropertyValues</a>
</td>
<td align="left" width="63%">
Retrieves a collection of alternates, which are a division of the alternate on which this method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451321">GetPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of a specified property of the alternate. Use this to obtain property values for <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">recogition properties</a> that have no corresponding helper property, such as the <a href="https://msdn.microsoft.com/4a27163b-e55a-4ced-8943-9a8ac161794c">Confidence</a> and <a href="https://msdn.microsoft.com/dd5578e7-7361-4e42-a503-2914f90a801f">LineNumber</a> properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25079651-4fcd-4f13-b73f-7d5ffefa871e">GetStrokesFromStrokeRanges</a>
</td>
<td align="left" width="63%">
Retrieves the smallest collection of <i>stroke</i> that contains a known input collection of strokes and for which the recognizer can provide alternates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dd8fa24-191f-465d-abd2-9a489df0324a">GetStrokesFromTextRange</a>
</td>
<td align="left" width="63%">
REtrieves the strokes collection that corresponds to the smallest set of that contains a specified character range within the alternate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b481e356-0a3c-4437-9700-6d8badcb0b0b">GetTextRangeFromStrokes</a>
</td>
<td align="left" width="63%">
Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionAlternate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4cc7bd86-e098-4de7-a73a-b878cba37e88">Ascender</a>


</td>
<td align="left" width="63%">
Gets the ascender line for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5fb53534-b15f-44e8-8bb3-31d6ba3a9bb4">Baseline</a>


</td>
<td align="left" width="63%">
Gets the baseline for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/049a5742-fc4f-4a9a-91d5-5eec56dc8e8b">Confidence</a>


</td>
<td align="left" width="63%">
Gets the level of confidence that a recognizer has in the recognition of an <b>IInkRecognitionAlternate</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ef3ab614-7aff-4660-bb2a-783f14e75b94">ConfidenceAlternates</a>


</td>
<td align="left" width="63%">
Gets the collection of alternates where the current alternate is split into a collection of smaller alternates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/52507911-b48c-47a9-8046-3000ed61e3c8">Descender</a>


</td>
<td align="left" width="63%">
Gets the descender line for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ccdf3092-b0a0-4626-b614-164548b1ca72">LineAlternates</a>


</td>
<td align="left" width="63%">
Gets the <b>IInkRecognitionAlternate</b> collection in which each alternate in the collection is on a separate line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dd5578e7-7361-4e42-a503-2914f90a801f">LineNumber</a>


</td>
<td align="left" width="63%">
Gets the line number that the recognition alternate corresponds to in the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ff12de3d-f760-4227-9406-634b19e66b4c">Midline</a>


</td>
<td align="left" width="63%">
Gets the midline for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1f603794-3b6a-4e8f-9804-fa4c85d82d1c">String</a>


</td>
<td align="left" width="63%">
Gets the result string of the alternate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/60ce6ed5-67d3-4471-a7a1-4653e8a122a1">Strokes</a>


</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that was used by the recognizer to generate the <b>IInkRecognitionAlternate</b> object.

</td>
</tr>
</table> 


## -remarks



A recognition segment is a basic ink fragment or unit that the recognizer uses internally to produce a recognition result for a known <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. The segments are usually determined by spacing and are broken down into the smallest possible ink fragments.

Sometimes the ink may have ambiguous distinctions between segments. These segments are compared to a recognizer's dictionary to determine possible matches (alternates). When the segments are compared, the recognizer creates a list of possible alternates and assigns a confidence level to each one, picking a top choice.

For instance, consider the phrase "how are you". This phrase is probably broken into three segments (depending on the spacing between segments), one for each word.

When each segment is recognized, a <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">RecognitionResult</a> is created. Each result then returns a list of alternates to choose from. For instance, the segment "how" may have alternates like "how", "now", "new", and so on, with "how" being the top alternate. By default, the top alternate is returned for each segment. You can choose to return alternates other than the top alternate.

You can also return alternates that are based on the properties of the alternates, such as the confidence level of the recognition result, the line number on which the alternates appear, and so on. See the <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty</a> object for a list of the recognition properties.

Alternates of alternates can also be returned.

Not all recognizers set all of the properties listed above. When an application attempts to access a property that is not set by the recognizer, an argument exception is thrown.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates Interface</a>



<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty Constants</a>
 

 

