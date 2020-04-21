---
UID: NN:shobjidl_core.IKnownFolderManager
title: IKnownFolderManager (shobjidl_core.h)
description: Exposes methods that create, enumerate or manage existing known folders.helpviewer_keywords: ["IKnownFolderManager","IKnownFolderManager interface [Windows Shell]","IKnownFolderManager interface [Windows Shell]","described","_shell_IKnownFolderManager","shell.IKnownFolderManager","shobjidl_core/IKnownFolderManager"]
old-location: shell\IKnownFolderManager.htm
tech.root: shell
ms.assetid: ba7dbef7-2732-49e8-b573-a3b731bdc633
ms.date: 12/05/2018
ms.keywords: IKnownFolderManager, IKnownFolderManager interface [Windows Shell], IKnownFolderManager interface [Windows Shell],described, _shell_IKnownFolderManager, shell.IKnownFolderManager, shobjidl_core/IKnownFolderManager
f1_keywords:
- shobjidl_core/IKnownFolderManager
dev_langs:
- c++
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
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IKnownFolderManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKnownFolderManager interface


## -description


Exposes methods that create, enumerate or manage existing known folders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKnownFolderManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKnownFolderManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-findfolderfromidlist">FindFolderFromIDList</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder based on an IDList. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-findfolderfrompath">FindFolderFromPath</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder based on a file system path. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-folderidfromcsidl">FolderIdFromCsidl</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that is the equivalent of a legacy <a href="https://docs.microsoft.com/windows/desktop/shell/csidl">CSIDL</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-folderidtocsidl">FolderIdToCsidl</a>
</td>
<td align="left" width="63%">
Gets the legacy <a href="https://docs.microsoft.com/windows/desktop/shell/csidl">CSIDL</a> value that is the equivalent of a given <a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolder">GetFolder</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder identified by its <a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderbyname">GetFolderByName</a>
</td>
<td align="left" width="63%">
Gets an object that represents a known folder identified by its canonical name. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids">GetFolderIds</a>
</td>
<td align="left" width="63%">
Gets an array of all registered known folder IDs. This can be used in enumerating all known folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect">Redirect</a>
</td>
<td align="left" width="63%">
Redirects folder requests for common and per-user folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder">RegisterFolder</a>
</td>
<td align="left" width="63%">
Adds a new known folder to the registry. Used particularly by ISVs that are adding one of their own folders to the known folder system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder">UnregisterFolder</a>
</td>
<td align="left" width="63%">
Remove a known folder from the registry, which makes it unknown to the known folder system. This method does not remove the folder itself.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
 

 

