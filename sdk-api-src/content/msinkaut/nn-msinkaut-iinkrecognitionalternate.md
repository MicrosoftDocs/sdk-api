---
UID: NN:msinkaut.IInkRecognitionAlternate
title: IInkRecognitionAlternate (msinkaut.h)

description: Represents the possible word matches for segments of ink that are compared to a recognizers dictionary.
old-location: tablet\iinkrecognitionalternate.htm
tech.root: tablet
ms.assetid: 219e96ee-6492-4f76-9928-f2e8dc28493d

ms.date: 12/05/2018
ms.keywords: 219e96ee-6492-4f76-9928-f2e8dc28493d, IInkRecognitionAlternate, IInkRecognitionAlternate interface [Tablet PC], IInkRecognitionAlternate interface [Tablet PC],described, msinkaut/IInkRecognitionAlternate, tablet.iinkrecognitionalternate
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkRecognitionAlternate"
dev_langs:
 - c++
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionAlternate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognitionAlternate interface


## -description



Represents the possible word matches for segments of ink that are compared to a recognizers dictionary.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionAlternate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognitionAlternate</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a>
</td>
<td align="left" width="63%">
Retrieves a collection of alternates, which are a division of the alternate on which this method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue">GetPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of a specified property of the alternate. Use this to obtain property values for <a href="https://docs.microsoft.com/windows/desktop/tablet/recognitionproperty-constants">recogition properties</a> that have no corresponding helper property, such as the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence">Confidence</a> and <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linenumber">LineNumber</a> properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getstrokesfromstrokeranges">GetStrokesFromStrokeRanges</a>
</td>
<td align="left" width="63%">
Retrieves the smallest collection of <i>stroke</i> that contains a known input collection of strokes and for which the recognizer can provide alternates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getstrokesfromtextrange">GetStrokesFromTextRange</a>
</td>
<td align="left" width="63%">
REtrieves the strokes collection that corresponds to the smallest set of that contains a specified character range within the alternate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-gettextrangefromstrokes">GetTextRangeFromStrokes</a>
</td>
<td align="left" width="63%">
Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_ascender">Ascender</a>


</td>
<td align="left" width="63%">
Gets the ascender line for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_baseline">Baseline</a>


</td>
<td align="left" width="63%">
Gets the baseline for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence">Confidence</a>


</td>
<td align="left" width="63%">
Gets the level of confidence that a recognizer has in the recognition of an <b>IInkRecognitionAlternate</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates">ConfidenceAlternates</a>


</td>
<td align="left" width="63%">
Gets the collection of alternates where the current alternate is split into a collection of smaller alternates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_descender">Descender</a>


</td>
<td align="left" width="63%">
Gets the descender line for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a>


</td>
<td align="left" width="63%">
Gets the <b>IInkRecognitionAlternate</b> collection in which each alternate in the collection is on a separate line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linenumber">LineNumber</a>


</td>
<td align="left" width="63%">
Gets the line number that the recognition alternate corresponds to in the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_midline">Midline</a>


</td>
<td align="left" width="63%">
Gets the midline for an <b>IInkRecognitionAlternate</b> object that represents a single line of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_string">String</a>


</td>
<td align="left" width="63%">
Gets the result string of the alternate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_strokes">Strokes</a>


</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that was used by the recognizer to generate the <b>IInkRecognitionAlternate</b> object.

</td>
</tr>
</table> 


## -remarks



A recognition segment is a basic ink fragment or unit that the recognizer uses internally to produce a recognition result for a known <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The segments are usually determined by spacing and are broken down into the smallest possible ink fragments.

Sometimes the ink may have ambiguous distinctions between segments. These segments are compared to a recognizer's dictionary to determine possible matches (alternates). When the segments are compared, the recognizer creates a list of possible alternates and assigns a confidence level to each one, picking a top choice.

For instance, consider the phrase "how are you". This phrase is probably broken into three segments (depending on the spacing between segments), one for each word.

When each segment is recognized, a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">RecognitionResult</a> is created. Each result then returns a list of alternates to choose from. For instance, the segment "how" may have alternates like "how", "now", "new", and so on, with "how" being the top alternate. By default, the top alternate is returned for each segment. You can choose to return alternates other than the top alternate.

You can also return alternates that are based on the properties of the alternates, such as the confidence level of the recognition result, the line number on which the alternates appear, and so on. See the <a href="https://docs.microsoft.com/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a> object for a list of the recognition properties.

Alternates of alternates can also be returned.

Not all recognizers set all of the properties listed above. When an application attempts to access a property that is not set by the recognizer, an argument exception is thrown.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty Constants</a>
 

 

