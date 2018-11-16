---
UID: NN:msinkaut.IInkCursorButtons
title: IInkCursorButtons
author: windows-sdk-content
description: Represents a collection of IInkCursorButton objects for an IInkCursor interface.
old-location: tablet\iinkcursorbuttons.htm
tech.root: tablet
ms.assetid: 3f695ab4-8174-402f-b7d6-810f149f5153
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 3f695ab4-8174-402f-b7d6-810f149f5153, IInkCursorButtons, IInkCursorButtons interface [Tablet PC], IInkCursorButtons interface [Tablet PC],described, msinkaut/IInkCursorButtons, tablet.iinkcursorbuttons
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
 - IInkCursorButtons
 - IInkCursorButtons._NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCursorButtons interface


## -description



Represents a collection of <a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton</a> objects for an <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkCursorButtons</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkCursorButtons</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/801cc3f5-3e30-48b9-bf1b-8dbfaff08dbf">Item</a>
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
Gets either the <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> or <a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a> enumerator interface for the collection. Use this property to retrieve each object in the collection.

The <b>_NewEnum</b>property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4c22d9bf-51a9-4c30-9e5d-ea166fce8bc8">Count</a>


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



You can use this collection to enumerate over the available <a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton</a> objects on a known <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> object.

For more information about collections in COM, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC APIs.




## -see-also




<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor Interface</a>



<a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton Interface</a>
 

 

