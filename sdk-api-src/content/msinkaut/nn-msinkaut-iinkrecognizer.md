---
UID: NN:msinkaut.IInkRecognizer
title: IInkRecognizer
author: windows-sdk-content
description: Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an InkRecognizerContext object, which is used to perform the actual handwriting recognition.
old-location: tablet\iinkrecognizer.htm
old-project: tablet
ms.assetid: 97f982b6-f330-4053-91a9-2a4edc13b4b0
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 97f982b6-f330-4053-91a9-2a4edc13b4b0, IInkRecognizer, IInkRecognizer interface [Tablet PC], IInkRecognizer interface [Tablet PC],described, msinkaut/IInkRecognizer, tablet.iinkrecognizer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognizer interface


## -description



Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object, which is used to perform the actual handwriting recognition.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognizer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRecognizer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b6aeec3f-8d57-4667-b171-1d8cad95f45c">CreateRecognizerContext</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> for the <b>IInkRecognizer</b>.

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

<a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities</a>


</td>
<td align="left" width="63%">
Gets the capabilities of the <b>IInkRecognizer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/96419ffa-6af1-4e45-a831-f11564501975">Languages</a>


</td>
<td align="left" width="63%">
Gets an array of language identifiers for the languages that the <b>IInkRecognizer</b> object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="63%">
Gets the name of the <b>IInkRecognizer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3486f667-a050-4063-99bf-09865d6edbda">PreferredPacketDescription</a>


</td>
<td align="left" width="63%">
Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/11153c7f-5284-483b-b1d5-01e670d924b4">SupportedProperties</a>


</td>
<td align="left" width="63%">
Gets an array of globally unique identifiers (GUIDs) that describe the properties that the <b>IInkRecognizer</b> object supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6b302453-ec9e-474b-b9ee-5776d464f4f8">Vendor</a>


</td>
<td align="left" width="63%">
Gets the vendor name of the recognizer object.

</td>
</tr>
</table> 


## -remarks



A recognizer has specific attributes and properties that allow it to perform recognition. The properties of a recognizer must be determined before recognition can occur. The types of properties that a recognizer supports determine the types of recognition it can perform. For instance, if a recognizer doesn't support cursive handwriting, it returns inaccurate results when a user writes in cursive.

A recognizer also has built-in functionality that automatically manages many aspects of handwriting. For instance, it determines the metrics for the lines on which strokes are drawn. You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.

For more information about recognition, see <a href="https://msdn.microsoft.com/614971a8-2b56-40d4-abb6-aba5ded01883">About Handwriting Recognition</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/b916e53f-9acd-40dc-961b-ebbecb15bd21">InkRecognizers Collection</a>
 

 

