---
UID: NN:directmanipulation.IDirectManipulationManager
title: IDirectManipulationManager
author: windows-sdk-content
description: Provides access to all the Direct Manipulation features and APIs available to the client application.
old-location: directmanipulation\idirectmanipulationmanager.htm
tech.root: directmanipulation
ms.assetid: d730a446-984e-4be0-aa7f-6d3dc93b2e34
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDirectManipulationManager, IDirectManipulationManager interface [Direct Manipulation], IDirectManipulationManager interface [Direct Manipulation],described, directmanipulation.idirectmanipulationmanager, directmanipulation/IDirectManipulationManager
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationManager interface


## -description



Provides access to all the <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> features and APIs available to the client application.



This is the first COM object (the object factory) created by the application to retrieve other COM objects in the <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> API surface. It also serves to activate and deactivate Direct Manipulation functionality on a per-HWND basis.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49a5eccd-16a9-4dca-af78-224fd5acb611">Activate</a>
</td>
<td align="left" width="63%">
Activates <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> for processing input and  handling callbacks on the specified window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8a2fbb2-f662-4eb7-88fb-64286205f19e">CreateContent</a>
</td>
<td align="left" width="63%">
The factory method that is used to create an instance of secondary content (such as a panning indicator) inside a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82a0146d-89c1-4672-93a9-e8f406b03d4e">CreateViewport</a>
</td>
<td align="left" width="63%">
The factory method that is used to create a new <a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f80fe8a-e088-41fa-b72e-2b248307ac4a">Deactivate</a>
</td>
<td align="left" width="63%">
Deactivates <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> for processing input and  handling callbacks on the specified window. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3080fcb-3bbe-492b-a94e-322f93781cf5">GetUpdateManager</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://msdn.microsoft.com/30626a22-1ded-49ff-a6c3-619a14d5ee3b">IDirectManipulationUpdateManager</a> object that receives compositor updates. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed7fa19b-acfe-4d5d-bd71-a77e5016fe68">ProcessInput</a>
</td>
<td align="left" width="63%">
Passes keyboard and mouse messages to the manipulation manager on the app's UI thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba71a959-b9b9-4466-9239-f3c486f5e7b3">RegisterHitTestTarget</a>
</td>
<td align="left" width="63%">
Registers a dedicated thread for hit testing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

