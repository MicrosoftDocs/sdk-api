---
UID: NN:msinkaut.IInkCursors
title: IInkCursors
author: windows-sdk-content
description: Represents a collection of IInkCursor objects.
old-location: tablet\iinkcursors.htm
tech.root: tablet
ms.assetid: 3ae7dbc4-e5a2-4916-a1cc-651659a008fc
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 3ae7dbc4-e5a2-4916-a1cc-651659a008fc, IInkCursors, IInkCursors interface [Tablet PC], IInkCursors interface [Tablet PC],described, msinkaut/IInkCursors, tablet.iinkcursors
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
 - IInkCursors
 - IInkCursors._NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCursors interface


## -description



Represents a collection of <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCursors</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkCursors</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkCursors</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59174954-4994-4773-acee-a3db363cb8fe">Item</a>
</td>
<td align="left" width="63%">
Specifies the cursor to return at the known index into the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCursors</b> interface has these properties.
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
Gets either the <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> or <a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b>property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/de036d87-32a2-4688-9926-d5f7ab965b9f">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of cursors in the collection.

</td>
</tr>
</table> 


## -remarks



A cursor becomes part of the cursors collection of an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, or the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control when it comes within range of the object. Each time a new cursor comes within range, it is added to the object's cursors collection. The cursors collection exists only during the lifetime of that object.

For example, if a pen is used to draw ink on an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, it becomes part of the <b>InkCollector</b> object's <a href="https://msdn.microsoft.com/6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4">Cursors</a> property. If a mouse is then used for input on the same <b>InkCollector</b> object, it is also added to the collection.

You can use this collection to enumerate over all of the <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> objects on a known <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object.

For more information about collections in COM, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor Interface</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>
 

 

