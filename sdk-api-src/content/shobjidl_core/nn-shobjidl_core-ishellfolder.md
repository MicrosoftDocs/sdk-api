---
UID: NN:shobjidl_core.IShellFolder
title: IShellFolder (shobjidl_core.h)
description: Exposed by all Shell namespace folder objects, its methods are used to manage folders.helpviewer_keywords: ["IShellFolder","IShellFolder interface [Windows Shell]","IShellFolder interface [Windows Shell]","described","_win32_IShellFolder","_win32_IShellFolder_cpp","shell.IShellFolder","shobjidl_core/IShellFolder"]
old-location: shell\IShellFolder.htm
tech.root: shell
ms.assetid: 35190a72-298b-4554-b924-e1357b583a99
ms.date: 12/05/2018
ms.keywords: IShellFolder, IShellFolder interface [Windows Shell], IShellFolder interface [Windows Shell],described, _win32_IShellFolder, _win32_IShellFolder_cpp, shell.IShellFolder, shobjidl_core/IShellFolder
f1_keywords:
- shobjidl_core/IShellFolder
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IShellFolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolder interface


## -description


Exposed by all Shell namespace folder objects, its methods are used to manage folders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">BindToObject</a>
</td>
<td align="left" width="63%">
Retrieves a handler, typically the Shell folder object that implements <b>IShellFolder</b> for a particular item. Optional parameters that control the construction of the handler are passed in the bind context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage">BindToStorage</a>
</td>
<td align="left" width="63%">
Requests a pointer to an object's storage interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">CompareIDs</a>
</td>
<td align="left" width="63%">
Determines the relative order of two file objects or folders, given their item identifier lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject">CreateViewObject</a>
</td>
<td align="left" width="63%">
Requests an object that can be used to obtain information from or interact with a folder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">EnumObjects</a>
</td>
<td align="left" width="63%">
Enables a client to determine the contents of a folder by creating an item identifier enumeration object and returning its <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> interface. The methods supported by that interface can then be used to enumerate the folder's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">GetAttributesOf</a>
</td>
<td align="left" width="63%">
Gets the attributes of one or more file or folder objects contained in the object represented by <b>IShellFolder</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">GetDisplayNameOf</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the specified file object or subfolder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">GetUIObjectOf</a>
</td>
<td align="left" width="63%">
Gets an object that can be used to carry out actions on the specified file objects or folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">ParseDisplayName</a>
</td>
<td align="left" width="63%">
Translates the display name of a file object or a folder into an item identifier list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof">SetNameOf</a>
</td>
<td align="left" width="63%">
Sets the display name of a file object or subfolder, changing the item identifier in the process.

</td>
</tr>
</table> 


## -remarks



Implement this interface for objects that extend the Shell's namespace. For example, implement this interface to create a separate namespace that requires a rooted Windows Explorer or to install a new namespace directly within the hierarchy of the system namespace. You are most familiar with the contents of your namespace, so you are responsible for implementing everything needed to access your data.

Use this interface when you need to display or perform an operation on the contents of the Shell's namespace. Objects that support <b>IShellFolder</b> are usually created by other Shell folder objects. To retrieve a folder's <b>IShellFolder</b> interface, you typically start by calling <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder">SHGetDesktopFolder</a>. This function returns a pointer to the desktop's <b>IShellFolder</b> interface. You can then use its methods to retrieve an <b>IShellFolder</b> interface for a particular namespace folder.

<div class="alert"><b>Note</b>  <b>IShellFolder</b> methods only accept PIDLs that are relative to the folder. Some <b>IShellFolder</b> methods, such as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>, only accept single-level PIDLs. In other words, the PIDL must contain only a single <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure, plus the terminating <b>NULL</b>. When you enumerate the contents of a folder with <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>, you will receive PIDLs of this form. Other methods, such as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">IShellFolder::CompareIDs</a>, accept multi-level PIDLs. These PIDLs can have multiple <b>SHITEMID</b> structures and identify objects one or more levels below the parent folder. Check the reference to be sure what type of PIDL can be accepted by a particular method.</div>
<div> </div>
<h3><a id="Examples"></a><a id="examples"></a><a id="EXAMPLES"></a>Examples</h3>
An example implementation of <b>IShellFolder</b> can be seen in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940360(v=vs.85)">Explorer Data Provider Sample</a> sample. The use of various <b>IShellFolder</b> methods can be found in several samples, including <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940361(v=vs.85)">File Operations Sample</a>.



