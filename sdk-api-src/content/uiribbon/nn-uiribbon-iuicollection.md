---
UID: NN:uiribbon.IUICollection
title: IUICollection
author: windows-sdk-content
description: The IUICollection interface is implemented by the Ribbon framework.
old-location: windowsribbon\windowsribbon_iuicollection.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\iuicollection.htm
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUICollection, IUICollection interface [Windows Ribbon], IUICollection interface [Windows Ribbon],described, scenicintent_IUICollection, uiribbon/IUICollection, windowsribbon.windowsribbon_iuicollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUICollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
req.product: Windows UI
---

# IUICollection interface


## -description


The <b>IUICollection</b> interface is implemented by the Ribbon framework. The <b>IUICollection</b> interface defines the 
		methods for dynamically manipulating collection-based controls, such as the various Ribbon <a href="https://msdn.microsoft.com/library/Dd742868(v=VS.85).aspx">galleries</a> and the 
		Quick Access Toolbar (QAT), at run time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUICollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUICollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUICollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the end of the <b>IUICollection</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Deletes all items from the <b>IUICollection</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items contained in the <b>IUICollection</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371513(v=VS.85).aspx">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves an item from the <b>IUICollection</b> at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371516(v=VS.85).aspx">Insert</a>
</td>
<td align="left" width="63%">
Inserts an item into the <b>IUICollection</b> at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597596">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes an item from the <b>IUICollection</b> at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371524(v=VS.85).aspx">Replace</a>
</td>
<td align="left" width="63%">
Replaces an item at the specified index of the <b>IUICollection</b> with another item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/Dd742704(v=VS.85).aspx">Gallery Sample</a>



<a href="https://msdn.microsoft.com/library/Dd371499(v=VS.85).aspx">IUICollectionChangedEvent</a>
 

 

