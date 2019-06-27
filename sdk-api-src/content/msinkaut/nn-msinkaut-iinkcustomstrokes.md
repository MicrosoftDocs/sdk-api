---
UID: NN:msinkaut.IInkCustomStrokes
title: IInkCustomStrokes (msinkaut.h)
author: windows-sdk-content
description: Contains a collection of user-defined InkStrokes collections.
old-location: tablet\iinkcustomstrokes.htm
tech.root: tablet
ms.assetid: 0b4eb5d6-ccf0-46c1-ae02-a393e67b817e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0b4eb5d6-ccf0-46c1-ae02-a393e67b817e, IInkCustomStrokes, IInkCustomStrokes interface [Tablet PC], IInkCustomStrokes interface [Tablet PC],described, msinkaut/IInkCustomStrokes, tablet.iinkcustomstrokes
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkCustomStrokes"
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
 - IInkCustomStrokes
 - IInkCustomStrokes._NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCustomStrokes interface


## -description



Contains a collection of user-defined <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCustomStrokes</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkCustomStrokes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkCustomStrokes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcustomstrokes-add">Add</a>
</td>
<td align="left" width="63%">
Specifies the collection of strokes to add to the collection of custom strokes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcustomstrokes-clear">Clear</a>
</td>
<td align="left" width="63%">
Specifies that all custom strokes are cleared from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcustomstrokes-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a> at the location specified within the <b>IInkCustomStrokes</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcustomstrokes-remove">Remove</a>
</td>
<td align="left" width="63%">
Specifies the collection of strokes to remove from the known collection of custom strokes.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCustomStrokes</b> interface has these properties.
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
Gets either the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b> property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcustomstrokes-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections within the collection of custom strokes.

</td>
</tr>
</table> 


## -remarks



The custom strokes are essentially named <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections that are persisted and recalled for later use.

You use a collection of custom strokes to store strokes that have the same meaning or that are related in some way. Examples of strokes that you may want to persist include:

<ul>
<li>All the strokes drawn by the same cursor (pen)</li>
<li>The strokes in an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that correspond to a word or paragraph</li>
<li>All the strokes that intersect a known region</li>
</ul>
For example, suppose you want to draw with two different cursors and keep separate the set of strokes that you draw with each cursor. You could recognize the strokes drawn with the first cursor and attach an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> object to that collection of strokes. To persist the recognition result, add the strokes to the <b>CustomStrokes</b> collection of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. You can later access the first collection of strokes by getting the persisted <b>CustomStrokes</b> collection from the <b>InkDisp</b> object.

Each <b>IInkCustomStrokes</b> collection is referenced by name.

<b>IInkCustomStrokes</b> collections are references to ink data, not the actual data itself.

For more information about collections in COM, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
 

 

