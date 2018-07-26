---
UID: NN:directmanipulation.IDirectManipulationUpdateManager
title: IDirectManipulationUpdateManager
author: windows-sdk-content
description: Manages how compositor updates are sent to Direct Manipulation.
old-location: directmanipulation\idirectmanipulationupdatemanager.htm
old-project: directmanipulation
ms.assetid: 30626a22-1ded-49ff-a6c3-619a14d5ee3b
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IDirectManipulationUpdateManager, IDirectManipulationUpdateManager interface [Direct Manipulation], IDirectManipulationUpdateManager interface [Direct Manipulation],described, directmanipulation.idirectmanipulationupdatemanager, directmanipulation/IDirectManipulationUpdateManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationUpdateManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationUpdateManager interface


## -description


Manages how compositor updates are sent to <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>.

This interface enables the compositor to trigger an update on <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> whenever there is a compositor update. The application should not call the methods of this interface directly.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationUpdateManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationUpdateManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationUpdateManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc0e22b8-ec27-478f-9c4b-ca192d8d52d0">RegisterWaitHandleCallback</a>
</td>
<td align="left" width="63%">
Registers a callback that is triggered by a handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d932a4a9-827f-4e23-b30a-3a4b85a60c6e">UnregisterWaitHandleCallback</a>
</td>
<td align="left" width="63%">
Deregisters a callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Updates <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> at the current time.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

