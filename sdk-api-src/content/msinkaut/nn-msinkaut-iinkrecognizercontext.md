---
UID: NN:msinkaut.IInkRecognizerContext
title: IInkRecognizerContext (msinkaut.h)
author: windows-sdk-content
description: "."
old-location: tablet\iinkrecognizercontext.htm
tech.root: tablet
ms.assetid: D3DC08E9-19CC-4281-9C71-CB9B8CBDDB7F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkRecognizerContext, IInkRecognizerContext interface [Tablet PC], IInkRecognizerContext interface [Tablet PC],described, msinkaut/IInkRecognizerContext, tablet.iinkrecognizercontext
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkRecognizerContext"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizerContext interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizerContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognizerContext</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-recognition">Recognition</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> has generated results from the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize</a> method.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-recognitionwithalternates">RecognitionWithAlternates</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a> has generated results after calling the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates">BackgroundRecognizeWithAlternates Method</a> method.
        

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
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize</a>
</td>
<td align="left" width="63%">
Causes the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-recognition">Recognition</a> event when recognition is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates">BackgroundRecognizeWithAlternates</a>
</td>
<td align="left" width="63%">
Causes the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-recognitionwithalternates">RecognitionWithAlternates</a> event when recognition is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput">EndInkInput</a>
</td>
<td align="left" width="63%">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput">EndInkInput</a> is no longer available for use for recognizers of western languages as of Windows Vista.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported">IsStringSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the system dictionary, user dictionary, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkwordlist-class">word list</a> contain a specified string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize">Recognize</a>
</td>
<td align="left" width="63%">
Performs recognition on an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and returns recognition results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition">StopBackgroundRecognition</a>
</td>
<td align="left" width="63%">
Ends background recognition that was started with a call to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates">BackgroundRecognizeWithAlternates</a>.

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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode">CharacterAutoCompletion</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid">Factoid</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide">Guide</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide</a> to use for ink input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext">PrefixText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the characters that come before the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer">Recognizer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object used by the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection associated with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext">SuffixText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the characters that come after the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist">WordList</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the word list that is used in the recognition process to improve the recognition results.

</td>
</tr>
</table> 

