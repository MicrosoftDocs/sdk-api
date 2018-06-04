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

# IShellFolderViewDual interface


## -description



			Exposes methods that modify the view and select items in the current folder.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewDual</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IShellFolderViewDual</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderViewDual</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d1a82fd-815d-4550-aaf4-662a6eeea287">get_Application</a>
</td>
<td align="left" width="63%">
Gets the application object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3e70cbe-51df-4749-8c6c-f3a43b33c436">get_FocusedItem</a>
</td>
<td align="left" width="63%">
Gets the FolderItem object that represents the item that has input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62af6b31-89bf-4965-a739-659f4fd932e3">get_Folder</a>
</td>
<td align="left" width="63%">
Gets the Folder object that represents the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36a893b3-6c4e-4cca-949b-707fd2aed125">get_Parent</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d683cda-0fe0-4984-b556-a6dd1223ca4c">get_Script</a>
</td>
<td align="left" width="63%">
Gets the scripting object for the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef3a163-bc38-40b2-aa3e-dcd36f87964f">get_ViewOptions</a>
</td>
<td align="left" width="63%">
Gets a set of flags that indicate the current options of the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f44e91b7-b651-4b6f-9583-cd9335ae6369">PopupItemMenu</a>
</td>
<td align="left" width="63%">
Creates a shortcut menu for the specified item and returns the selected command string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71ec6c0d-f3de-4a5d-941b-16d33b718921">SelectedItems</a>
</td>
<td align="left" width="63%">
Gets a FolderItems object that represents all of the selected items in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9bc12f-bf5f-42f2-a1cd-160298f7c73a">SelectItem</a>
</td>
<td align="left" width="63%">
Sets the selection state of an item in the view.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/f53b779e-a015-4b17-b04d-e0739cba8168">IShellFolderViewDual2</a>



<a href="https://msdn.microsoft.com/1aa70db8-4225-49de-8b8f-ec86b1aafa22">IShellFolderViewDual3</a>
 

 

