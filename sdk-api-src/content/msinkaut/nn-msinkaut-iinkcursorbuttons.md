---
UID: NN:msinkaut.IInkCursorButtons
title: IInkCursorButtons (msinkaut.h)
author: windows-sdk-content
description: Represents a collection of IInkCursorButton objects for an IInkCursor interface.
old-location: tablet\iinkcursorbuttons.htm
tech.root: tablet
ms.assetid: 3f695ab4-8174-402f-b7d6-810f149f5153
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3f695ab4-8174-402f-b7d6-810f149f5153, IInkCursorButtons, IInkCursorButtons interface [Tablet PC], IInkCursorButtons interface [Tablet PC],described, msinkaut/IInkCursorButtons, tablet.iinkcursorbuttons
ms.topic: interface
f1_keywords: ["msinkaut/IInkCursorButtons"]
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
 - IInkCursorButtons
 - IInkCursorButtons._NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCursorButtons interface


## -description



Represents a collection of <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> objects for an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCursorButtons</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkCursorButtons</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkCursorButtons</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursorbuttons-item">Item</a>
</td>
<td align="left" width="63%">
Specifies the cursor button to return at the known index in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCursorButtons</b> interface has these properties.
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

The <b>_NewEnum</b>property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursorbuttons-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of cursor buttons in the collection.

</td>
</tr>
</table> 


## -remarks



You can use this collection to enumerate over the available <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> objects on a known <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object.

For more information about collections in COM, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC APIs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton Interface</a>
 

 

