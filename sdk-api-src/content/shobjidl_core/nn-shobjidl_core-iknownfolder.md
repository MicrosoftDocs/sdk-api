---
UID: NN:shobjidl_core.IKnownFolder
title: IKnownFolder
author: windows-sdk-content
description: Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, pointer to an item identifier list (PIDL) value, redirection capabilities, and definition.
old-location: shell\IKnownFolder.htm
tech.root: Shell
ms.assetid: dbade93d-73f6-401b-9986-4e6fd439c874
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IKnownFolder, IKnownFolder interface [Windows Shell], IKnownFolder interface [Windows Shell],described, _shell_IKnownFolder, shell.IKnownFolder, shobjidl_core/IKnownFolder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder interface


## -description


Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, pointer to an item identifier list (PIDL) value, redirection capabilities, and definition. It provides a method for the retrival of a known folder's <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object. It also provides methods to get or set the path of the known folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKnownFolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKnownFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKnownFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3a7f249-9d57-4bd1-830f-1c83c745782f">GetCategory</a>
</td>
<td align="left" width="63%">
Retrieves the category—virtual, fixed, common, or per-user—of the selected folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6f544cc-f487-405c-915d-b3a6dc59422c">GetFolderDefinition</a>
</td>
<td align="left" width="63%">
Retrieves a structure that contains the defining elements of a known folder, which includes the folder's category, name, path, description, tooltip, icon, and other properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2457d52-390d-43bd-8db0-9c18492cc40e">GetFolderType</a>
</td>
<td align="left" width="63%">
Retrieves the folder type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c20fc32f-394d-4fbe-b7dd-072d84be2713">GetId</a>
</td>
<td align="left" width="63%">
Gets the ID of the selected folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1c77198-da52-4f74-9e20-56b6d1d450f5">GetIDList</a>
</td>
<td align="left" width="63%">
Gets the location of the Shell namespace folder in the IDList (<a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>) form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1786db0-9bcc-4fc8-ae18-8519da6edda9">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the path of a known folder as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5abc4944-1fd7-400a-817d-b58a7f4989ea">GetRedirectionCapabilities</a>
</td>
<td align="left" width="63%">
Gets a value that states whether the known folder can have its path set to a new value or what specific restrictions or prohibitions are placed on that redirection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a42c0a20-9c72-48d3-8432-15b73ff211d2">GetShellItem</a>
</td>
<td align="left" width="63%">
Retrieves the location of a known folder in the Shell namespace in the form of a Shell item (<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or derived interface).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/235f69de-3571-4184-aa52-b409fbc1d643">SetPath</a>
</td>
<td align="left" width="63%">
Assigns a new path to a known folder.

</td>
</tr>
</table> 


## -remarks



<b>IKnownFolder</b> objects can be obtained through several methods of the <a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a> interface, such as <a href="https://msdn.microsoft.com/bd8dba51-c711-4f7c-af53-00c80f211cb8">IKnownFolderManager::GetFolder</a> and <a href="https://msdn.microsoft.com/fda3e390-e436-47ab-9339-2abf30b53ba9">IKnownFolderManager::FindFolderFromIDList</a>.

Third parties do not implement <b>IKnownFolder</b>. Use the provided implementation.




## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

