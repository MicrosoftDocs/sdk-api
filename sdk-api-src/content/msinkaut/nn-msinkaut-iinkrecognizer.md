---
UID: NN:msinkaut.IInkRecognizer
title: IInkRecognizer (msinkaut.h)
description: Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an InkRecognizerContext object, which is used to perform the actual handwriting recognition.
old-location: tablet\iinkrecognizer.htm
tech.root: tablet
ms.assetid: 97f982b6-f330-4053-91a9-2a4edc13b4b0
ms.date: 12/05/2018
ms.keywords: 97f982b6-f330-4053-91a9-2a4edc13b4b0, IInkRecognizer, IInkRecognizer interface [Tablet PC], IInkRecognizer interface [Tablet PC],described, msinkaut/IInkRecognizer, tablet.iinkrecognizer
f1_keywords:
- msinkaut/IInkRecognizer
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
- IInkRecognizer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizer interface


## -description



Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object, which is used to perform the actual handwriting recognition.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognizer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkRecognizer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext">CreateRecognizerContext</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> for the <b>IInkRecognizer</b>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities</a>


</td>
<td align="left" width="63%">
Gets the capabilities of the <b>IInkRecognizer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages">Languages</a>


</td>
<td align="left" width="63%">
Gets an array of language identifiers for the languages that the <b>IInkRecognizer</b> object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name">Name</a>


</td>
<td align="left" width="63%">
Gets the name of the <b>IInkRecognizer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_preferredpacketdescription">PreferredPacketDescription</a>


</td>
<td align="left" width="63%">
Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_supportedproperties">SupportedProperties</a>


</td>
<td align="left" width="63%">
Gets an array of globally unique identifiers (GUIDs) that describe the properties that the <b>IInkRecognizer</b> object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_vendor">Vendor</a>


</td>
<td align="left" width="63%">
Gets the vendor name of the recognizer object.

</td>
</tr>
</table> 


## -remarks



A recognizer has specific attributes and properties that allow it to perform recognition. The properties of a recognizer must be determined before recognition can occur. The types of properties that a recognizer supports determine the types of recognition it can perform. For instance, if a recognizer doesn't support cursive handwriting, it returns inaccurate results when a user writes in cursive.

A recognizer also has built-in functionality that automatically manages many aspects of handwriting. For instance, it determines the metrics for the lines on which strokes are drawn. You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.

For more information about recognition, see <a href="https://docs.microsoft.com/windows/desktop/tablet/about-handwriting-recognition">About Handwriting Recognition</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)">InkRecognizers Collection</a>
 

 

