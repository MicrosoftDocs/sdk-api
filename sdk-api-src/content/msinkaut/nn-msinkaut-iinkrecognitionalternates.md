---
UID: NN:msinkaut.IInkRecognitionAlternates
title: IInkRecognitionAlternates
author: windows-sdk-content
description: Contains the IInkRecognitionAlternate objects that represent possible word matches for segments of ink.
old-location: tablet\iinkrecognitionalternates.htm
tech.root: tablet
ms.assetid: 39f49762-de86-4a1a-ac7b-327b65c3eb54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 39f49762-de86-4a1a-ac7b-327b65c3eb54, IInkRecognitionAlternates, IInkRecognitionAlternates interface [Tablet PC], IInkRecognitionAlternates interface [Tablet PC],described, msinkaut/IInkRecognitionAlternates, tablet.iinkrecognitionalternates
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInkRecognitionAlternates
 - IInkRecognitionAlternates._NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognitionAlternates interface


## -description



Contains the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> objects that represent possible word matches for segments of ink.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionAlternates</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRecognitionAlternates</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkRecognitionAlternates</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63a00f6d-f733-4b25-bfe2-4f841b9694fa">Item</a>
</td>
<td align="left" width="63%">
Specifies the alternate at the known index in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionAlternates</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>_NewEnum</b>

</td>
<td align="left" width="10%">


</td>
<td align="left" width="63%">
Gets either the <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> or <a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b> property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2bcca92c-ba9f-437f-b7a9-6056da243d1a">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of alternates in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ce483ea1-4b66-4a87-89a7-f71feae8ccc4">Strokes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the strokes that were used to create the collection.

</td>
</tr>
</table> 


## -remarks



For more information about collections in COM, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

