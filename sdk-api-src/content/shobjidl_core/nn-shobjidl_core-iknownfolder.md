---
UID: NN:shobjidl_core.IKnownFolder
title: IKnownFolder (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, pointer to an item identifier list (PIDL) value, redirection capabilities, and definition.
old-location: shell\IKnownFolder.htm
tech.root: shell
ms.assetid: dbade93d-73f6-401b-9986-4e6fd439c874
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKnownFolder, IKnownFolder interface [Windows Shell], IKnownFolder interface [Windows Shell],described, _shell_IKnownFolder, shell.IKnownFolder, shobjidl_core/IKnownFolder
ms.topic: interface
f1_keywords: ["shobjidl_core/IKnownFolder"]
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
ms.custom: 19H1
---

# IKnownFolder interface


## -description


Exposes methods that allow an application to retrieve information about a known folder's category, type, GUID, pointer to an item identifier list (PIDL) value, redirection capabilities, and definition. It provides a method for the retrival of a known folder's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object. It also provides methods to get or set the path of the known folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKnownFolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKnownFolder</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getcategory">GetCategory</a>
</td>
<td align="left" width="63%">
Retrieves the category—virtual, fixed, common, or per-user—of the selected folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition">GetFolderDefinition</a>
</td>
<td align="left" width="63%">
Retrieves a structure that contains the defining elements of a known folder, which includes the folder's category, name, path, description, tooltip, icon, and other properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfoldertype">GetFolderType</a>
</td>
<td align="left" width="63%">
Retrieves the folder type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid">GetId</a>
</td>
<td align="left" width="63%">
Gets the ID of the selected folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist">GetIDList</a>
</td>
<td align="left" width="63%">
Gets the location of the Shell namespace folder in the IDList (<a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a>) form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the path of a known folder as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities">GetRedirectionCapabilities</a>
</td>
<td align="left" width="63%">
Gets a value that states whether the known folder can have its path set to a new value or what specific restrictions or prohibitions are placed on that redirection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getshellitem">GetShellItem</a>
</td>
<td align="left" width="63%">
Retrieves the location of a known folder in the Shell namespace in the form of a Shell item (<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or derived interface).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath">SetPath</a>
</td>
<td align="left" width="63%">
Assigns a new path to a known folder.

</td>
</tr>
</table> 


## -remarks



<b>IKnownFolder</b> objects can be obtained through several methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a> interface, such as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolder">IKnownFolderManager::GetFolder</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-findfolderfromidlist">IKnownFolderManager::FindFolderFromIDList</a>.

Third parties do not implement <b>IKnownFolder</b>. Use the provided implementation.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
 

 

