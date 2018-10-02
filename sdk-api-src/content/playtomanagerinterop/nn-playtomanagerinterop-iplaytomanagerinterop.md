---
UID: NN:playtomanagerinterop.IPlayToManagerInterop
title: IPlayToManagerInterop
author: windows-sdk-content
description: Enables access to PlayToManager methods in a Windows Store app that manages multiple windows.
old-location: winrt\iplaytomanagerinterop.htm
tech.root: WinRT
ms.assetid: e7a8df61-e5ae-4eff-a4eb-e0a5cdae3b7f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPlayToManagerInterop, IPlayToManagerInterop interface [Windows Runtime], IPlayToManagerInterop interface [Windows Runtime],described, playtomanagerinterop/IPlayToManagerInterop, winrt.iplaytomanagerinterop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: playtomanagerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Playtomanagerinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - playtomanagerinterop.h
api_name:
 - IPlayToManagerInterop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPlayToManagerInterop interface


## -description


Enables access to <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> methods in a Windows Store app that manages multiple windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlayToManagerInterop</b> interface inherits from <b>IInspectable</b>. <b>IPlayToManagerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPlayToManagerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/444f0d68-a6ae-46de-aa97-d7d505c95948">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a> instance for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/106ddd95-06dd-479a-8350-39d791add469">ShowPlayToUIForWindow</a>
</td>
<td align="left" width="63%">
Displays the Play To UI for the specified window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e5de08a6-cc89-4422-bfe7-f170b8ec4412">PlayToManager</a>
 

 

