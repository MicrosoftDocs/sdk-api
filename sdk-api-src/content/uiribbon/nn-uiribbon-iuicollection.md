---
UID: NN:uiribbon.IUICollection
title: IUICollection (uiribbon.h)
author: windows-sdk-content
description: The IUICollection interface is implemented by the Ribbon framework.
old-location: windowsribbon\windowsribbon_iuicollection.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\iuicollection.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUICollection, IUICollection interface [Windows Ribbon], IUICollection interface [Windows Ribbon],described, scenicintent_IUICollection, uiribbon/IUICollection, windowsribbon.windowsribbon_iuicollection
ms.topic: interface
f1_keywords: 
 - "uiribbon/IUICollection"
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
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUICollection interface


## -description


The <b>IUICollection</b> interface is implemented by the Ribbon framework. The <b>IUICollection</b> interface defines the 
		methods for dynamically manipulating collection-based controls, such as the various Ribbon <a href="https://docs.microsoft.com/windows/desktop/windowsribbon/ribbon-controls-galleries">galleries</a> and the 
		Quick Access Toolbar (QAT), at run time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUICollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUICollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the end of the <b>IUICollection</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Deletes all items from the <b>IUICollection</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items contained in the <b>IUICollection</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves an item from the <b>IUICollection</b> at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-insert">Insert</a>
</td>
<td align="left" width="63%">
Inserts an item into the <b>IUICollection</b> at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-removeat">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes an item from the <b>IUICollection</b> at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollection-replace">Replace</a>
</td>
<td align="left" width="63%">
Replaces an item at the specified index of the <b>IUICollection</b> with another item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent">IUICollectionChangedEvent</a>
 

 

