---
UID: NN:uiribbon.IUIApplication
title: IUIApplication (uiribbon.h)
author: windows-sdk-content
description: The IUIApplication interface is implemented by the application and defines the callback entry-point methods for the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuiapplication.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiapplication\iuiapplication.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIApplication, IUIApplication interface [Windows Ribbon], IUIApplication interface [Windows Ribbon],described, scenicintent_IUIApplication, uiribbon/IUIApplication, windowsribbon.windowsribbon_iuiapplication
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
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Dd371531(v=VS.85).aspx">OnCreateUICommand</a>
</td>
<td align="left" width="63%">
Called for each Command specified in the Ribbon framework markup to bind the Command to an <a href="https://msdn.microsoft.com/en-us/library/Dd371491(v=VS.85).aspx">IUICommandHandler</a>.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd371534(v=VS.85).aspx">OnDestroyUICommand</a>
</td>
<td align="left" width="63%">
Called for each Command specified in the Ribbon framework markup when the application window is destroyed.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd371537(v=VS.85).aspx">OnViewChanged</a>
</td>
<td align="left" width="63%">
Called when the state of a  <a href="https://msdn.microsoft.com/en-us/library/Dd371600(v=VS.85).aspx">View</a> changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

