---
UID: NN:uiribbon.IUIApplication
title: IUIApplication
author: windows-sdk-content
description: The IUIApplication interface is implemented by the application and defines the callback entry-point methods for the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuiapplication.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiapplication\iuiapplication.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIApplication, IUIApplication interface [Windows Ribbon], IUIApplication interface [Windows Ribbon],described, scenicintent_IUIApplication, uiribbon/IUIApplication, windowsribbon.windowsribbon_iuiapplication
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIApplication interface


## -description


The <b>IUIApplication</b> interface is implemented by the application and defines the callback entry-point methods for the Windows Ribbon framework.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIApplication</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13e03acd-1a1e-48f9-b413-5a24d8b784d0">OnCreateUICommand</a>
</td>
<td align="left" width="63%">
Called for each Command specified in the Ribbon framework markup to bind the Command to an <a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c25f2279-1227-4ce2-9787-c046479b3a33">OnDestroyUICommand</a>
</td>
<td align="left" width="63%">
Called for each Command specified in the Ribbon framework markup when the application window is destroyed.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9672131d-bc7a-4e7b-935e-cd38dff2bb5c">OnViewChanged</a>
</td>
<td align="left" width="63%">
Called when the state of a  <a href="https://msdn.microsoft.com/e7549b8b-0f95-477a-9024-1a99ee1412c2">View</a> changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

