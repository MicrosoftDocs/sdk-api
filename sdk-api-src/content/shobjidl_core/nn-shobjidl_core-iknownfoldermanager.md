---
UID: NN:shobjidl_core.IKnownFolderManager
title: IKnownFolderManager
author: windows-sdk-content
description: Exposes methods that create, enumerate or manage existing known folders.
old-location: shell\IKnownFolderManager.htm
old-project: shell
ms.assetid: ba7dbef7-2732-49e8-b573-a3b731bdc633
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IKnownFolderManager, IKnownFolderManager interface [Windows Shell], IKnownFolderManager interface [Windows Shell],described, _shell_IKnownFolderManager, shell.IKnownFolderManager, shobjidl_core/IKnownFolderManager
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolderManager
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IKnownFolderManager interface


## -description


Exposes methods that create, enumerate or manage existing known folders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKnownFolderManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKnownFolderManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKnownFolderManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fda3e390-e436-47ab-9339-2abf30b53ba9">FindFolderFromIDList</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder based on an IDList. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8033305-e5b9-499d-b794-ac3190141650">FindFolderFromPath</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder based on a file system path. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c819558-8cbd-4576-98e6-99efa39ca5a6">FolderIdFromCsidl</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that is the equivalent of a legacy <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27bd8c79-34ff-44ee-ad99-aa079af7da89">FolderIdToCsidl</a>
</td>
<td align="left" width="63%">
Gets the legacy <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value that is the equivalent of a given <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd8dba51-c711-4f7c-af53-00c80f211cb8">GetFolder</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder identified by its <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfabc06c-825d-488d-919e-4cd9109eae52">GetFolderByName</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder identified by its canonical name. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ac09fc4-15c4-4346-94ad-2a4617c463d1">GetFolderIds</a>
</td>
<td align="left" width="63%">
Gets an array of all registered known folder IDs. This can be used in enumerating all known folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f4fc609-597b-4c72-b875-4b3f051dd056">Redirect</a>
</td>
<td align="left" width="63%">
Redirects folder requests for common and per-user folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b3d492f-26a3-4f04-ba01-768ebad39e1b">RegisterFolder</a>
</td>
<td align="left" width="63%">
Adds a new known folder to the registry. Used particularly by ISVs that are adding one of their own folders to the known folder system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c66f5e3-3479-414c-8888-0a888708dbe0">UnregisterFolder</a>
</td>
<td align="left" width="63%">
Remove a known folder from the registry, which makes it unknown to the known folder system. This method does not remove the folder itself.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

