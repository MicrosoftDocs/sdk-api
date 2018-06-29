---
UID: NN:uiribbon.IUIFramework
title: IUIFramework
author: windows-sdk-content
description: The IUIFramework interface is implemented by the Windows Ribbon framework and defines the methods that provide the core functionality for the framework.
old-location: windowsribbon\windowsribbon_iuiframework.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\iuiframework.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IUIFramework, IUIFramework interface [Windows Ribbon], IUIFramework interface [Windows Ribbon],described, scenicintent_IUIFramework, uiribbon/IUIFramework, windowsribbon.windowsribbon_iuiframework
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
 - IUIFramework
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
req.product: Windows UI
---

# IUIFramework interface


## -description



			
				The <b>IUIFramework</b> interface is implemented by the Windows Ribbon framework and defines the methods that provide the core functionality for the framework.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIFramework</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIFramework</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIFramework</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371368(v=VS.85).aspx">Destroy</a>
</td>
<td align="left" width="63%">
Terminates and releases all objects, hooks, and references for an instance of the Ribbon framework. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371369(v=VS.85).aspx">FlushPendingInvalidations</a>
</td>
<td align="left" width="63%">

			Processes all pending Command updates.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371370(v=VS.85).aspx">GetUICommandProperty</a>
</td>
<td align="left" width="63%">

			Retrieves a command property, value, or state.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371371(v=VS.85).aspx">GetView</a>
</td>
<td align="left" width="63%">

			Retrieves the address of a pointer to an interface that represents a Ribbon framework View, such as <a href="https://msdn.microsoft.com/library/Dd371360(v=VS.85).aspx">IUIRibbon</a> 
			or <a href="https://msdn.microsoft.com/library/Dd371482(v=VS.85).aspx">IUIContextualUI</a>.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Connects the host application to the Ribbon framework.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371375(v=VS.85).aspx">InvalidateUICommand</a>
</td>
<td align="left" width="63%">

			Invalidates a Ribbon framework Command property, value, or state. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371471(v=VS.85).aspx">LoadUI</a>
</td>
<td align="left" width="63%">

			Loads the Ribbon framework UI resource, or compiled markup, file.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371476(v=VS.85).aspx">SetModes</a>
</td>
<td align="left" width="63%">

			Specifies the application modes to enable. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Dd371478(v=VS.85).aspx">SetUICommandProperty</a>
</td>
<td align="left" width="63%">

			Sets a command property, value, or state.
		

</td>
</tr>
</table> 


## -remarks



This interface is used to initialize and dismantle the Ribbon framework.

Ribbon framework UI functionality is differentiated by Views, which are essentially 
				built-in core controls, such as the <a href="https://msdn.microsoft.com/library/Dd316811(v=VS.85).aspx">Ribbon</a> and <a href="https://msdn.microsoft.com/library/Dd371654(v=VS.85).aspx">ContextPopup</a>.

To get an interface pointer to the implementation of IUIFramework, use <a href="http://go.microsoft.com/fwlink/p/?linkid=199586">CoCreateInstance</a>
		 to 
			create a COM object with the class identifier (CLSID) of CLSID_UIRibbonFramework.
			




## -see-also




<a href="https://msdn.microsoft.com/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

