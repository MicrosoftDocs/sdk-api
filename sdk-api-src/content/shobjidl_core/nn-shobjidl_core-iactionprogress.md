---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IActionProgress interface


## -description


Represents the abstract base class from which progress-driven operations can inherit.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActionProgress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IActionProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActionProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c26dd072-6d59-4c6c-a273-682ded994612">Begin</a>
</td>
<td align="left" width="63%">
Called when an action has begun that requires its progress be displayed to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91fa11c3-c781-4e96-9a42-4625b8b24333">End</a>
</td>
<td align="left" width="63%">
Indicates that the action associated with this progress implementation has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5db4344-c1b4-4e76-9291-46dafc82e88d">QueryCancel</a>
</td>
<td align="left" width="63%">
Provides information about whether the action is being canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28a2ee51-0a7a-4802-be55-f111be3a4d2d">ResetCancel</a>
</td>
<td align="left" width="63%">
Resets progress dialog after a cancellation has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9c6fd82-96a2-4021-a6c4-ab61e20eb0d0">UpdateProgress</a>
</td>
<td align="left" width="63%">

      Updates the progress of an action to the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfb8a996-89df-4975-ac13-d871598a2787">UpdateText</a>
</td>
<td align="left" width="63%">
Called if descriptive text associated with the action will be changed.

</td>
</tr>
</table> 


## -remarks



This class is an abstract class that may not be instantiated. It provides a framework that derived classes can use to implement a progress callback. This callback can be used by applications to report progress of actions to the UI. Here, "Actions" refers to operations that may take a significant amount of time, such as downloading or copying files, and during which a visible progress indication would be appropriate.

Applications typically do not implement this interface. Much of the functionality that users interact with during actions is provided by the CProgressDialog class (CLSID_ProgressDialog) that implements <b>IActionProgress</b> and displays progress in a dialog box. If a solution requiring a mechanism other than a dialog box is required, <b>IActionProgress</b> can be used to provide basic progress indicator functionality.

Once implemented, classes should call <a href="https://msdn.microsoft.com/c26dd072-6d59-4c6c-a273-682ded994612">IActionProgress::Begin</a> when an action is started. Periodically, <a href="https://msdn.microsoft.com/d9c6fd82-96a2-4021-a6c4-ab61e20eb0d0">IActionProgress::UpdateProgress</a> should be called to update the UI with progress information, and detailed textual information should be conveyed to the UI by calling <a href="https://msdn.microsoft.com/dfb8a996-89df-4975-ac13-d871598a2787">IActionProgress::UpdateText</a>. <a href="https://msdn.microsoft.com/a5db4344-c1b4-4e76-9291-46dafc82e88d">IActionProgress::QueryCancel</a> and <a href="https://msdn.microsoft.com/28a2ee51-0a7a-4802-be55-f111be3a4d2d">IActionProgress::ResetCancel</a> should be called to handle cancellation requests. Once the operation ends, <a href="https://msdn.microsoft.com/91fa11c3-c781-4e96-9a42-4625b8b24333">IActionProgress::End</a> should be called.




## -see-also




<a href="https://msdn.microsoft.com/ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb">IProgressDialog</a>
 

 

