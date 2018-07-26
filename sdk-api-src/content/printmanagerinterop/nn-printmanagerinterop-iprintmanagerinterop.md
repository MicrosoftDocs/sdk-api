---
UID: NN:printmanagerinterop.IPrintManagerInterop
title: IPrintManagerInterop
author: windows-sdk-content
description: Enables access to PrintManager methods in a Windows Store app that manages multiple windows.
old-location: winrt\iprintmanagerinterop.htm
old-project: WinRT
ms.assetid: 1786fda1-37e4-4ec5-94de-a1fc5b6732a2
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IPrintManagerInterop, IPrintManagerInterop interface [Windows Runtime], IPrintManagerInterop interface [Windows Runtime],described, printmanagerinterop/IPrintManagerInterop, winrt.iprintmanagerinterop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: printmanagerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Printmanagerinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USER_POWER_POLICY, *PUSER_POWER_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - printmanagerinterop.h
api_name:
 - IPrintManagerInterop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPrintManagerInterop interface


## -description


Enables access to <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> methods in a Windows Store app that manages multiple windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintManagerInterop</b> interface inherits from <b>IInspectable</b>. <b>IPrintManagerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintManagerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cbf37b6-6756-4399-aa6b-01eb63c8c6db">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a> instance for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2414279e-e1ef-48c7-87a1-a09ad367aec4">ShowPrintUIForWindowAsync</a>
</td>
<td align="left" width="63%">
Displays the UI for printing content for the specified window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a>
 

 

