---
UID: NN:uiribbon.IUISimplePropertySet
title: IUISimplePropertySet
author: windows-sdk-content
description: IUISimplePropertySet is a read-only interface that defines a method for retrieving the value identified by a property key.
old-location: windowsribbon\windowsribbon_iuisimplepropertyset.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuisimplepropertyset\iuisimplepropertyset.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUISimplePropertySet, IUISimplePropertySet interface [Windows Ribbon], IUISimplePropertySet interface [Windows Ribbon],described, scenicintent_IUISimplePropertySet, uiribbon/IUISimplePropertySet, windowsribbon.windowsribbon_iuisimplepropertyset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiribbon.h
req.include-header: 
req.redist: 
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
 - IUISimplePropertySet
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
req.product: Windows UI
---

# IUISimplePropertySet interface


## -description


<b>IUISimplePropertySet</b> is a read-only interface that defines a method for retrieving the value identified by a  property key. This interface is implemented by the Windows Ribbon framework and is also implemented by  the host application for each item in the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a> object of an item gallery.

When implemented by the host application, the method defined by this interface is used to retrieve a property key  value for the selected item in the <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUISimplePropertySet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUISimplePropertySet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUISimplePropertySet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d62ce1c-58ac-47a0-8b06-57655e18c982">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value identified by a property key.
		

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/12bc7fda-ff69-4316-8baf-cc97e19a231c">Property Keys</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>



<a href="https://msdn.microsoft.com/447039f3-1428-4b6f-94cf-78cf81974041">Working with Galleries</a>
 

 

