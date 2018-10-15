---
UID: NN:shobjidl_core.IShellFolder
title: IShellFolder
author: windows-sdk-content
description: Exposed by all Shell namespace folder objects, its methods are used to manage folders.
old-location: shell\IShellFolder.htm
tech.root: shell
ms.assetid: 35190a72-298b-4554-b924-e1357b583a99
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IShellFolder, IShellFolder interface [Windows Shell], IShellFolder interface [Windows Shell],described, _win32_IShellFolder, _win32_IShellFolder_cpp, shell.IShellFolder, shobjidl_core/IShellFolder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolder interface


## -description


Exposed by all Shell namespace folder objects, its methods are used to manage folders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellFolder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">BindToObject</a>
</td>
<td align="left" width="63%">
Retrieves a handler, typically the Shell folder object that implements <b>IShellFolder</b> for a particular item. Optional parameters that control the construction of the handler are passed in the bind context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6abd12bb-5c85-4f3b-a6ad-a7c05ce02ce3">BindToStorage</a>
</td>
<td align="left" width="63%">
Requests a pointer to an object's storage interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">CompareIDs</a>
</td>
<td align="left" width="63%">
Determines the relative order of two file objects or folders, given their item identifier lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a1b73ad-6719-403a-a8aa-27bef537b7a9">CreateViewObject</a>
</td>
<td align="left" width="63%">
Requests an object that can be used to obtain information from or interact with a folder object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/248bec8b-0bf4-47d5-adb3-31a685a2c359">EnumObjects</a>
</td>
<td align="left" width="63%">
Enables a client to determine the contents of a folder by creating an item identifier enumeration object and returning its <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a> interface. The methods supported by that interface can then be used to enumerate the folder's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">GetAttributesOf</a>
</td>
<td align="left" width="63%">
Gets the attributes of one or more file or folder objects contained in the object represented by <b>IShellFolder</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">GetDisplayNameOf</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the specified file object or subfolder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">GetUIObjectOf</a>
</td>
<td align="left" width="63%">
Gets an object that can be used to carry out actions on the specified file objects or folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">ParseDisplayName</a>
</td>
<td align="left" width="63%">
Translates the display name of a file object or a folder into an item identifier list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b975df89-9289-4344-9c55-f11ee83229dd">SetNameOf</a>
</td>
<td align="left" width="63%">
Sets the display name of a file object or subfolder, changing the item identifier in the process.

</td>
</tr>
</table> 


## -remarks



Implement this interface for objects that extend the Shell's namespace. For example, implement this interface to create a separate namespace that requires a rooted Windows Explorer or to install a new namespace directly within the hierarchy of the system namespace. You are most familiar with the contents of your namespace, so you are responsible for implementing everything needed to access your data.

Use this interface when you need to display or perform an operation on the contents of the Shell's namespace. Objects that support <b>IShellFolder</b> are usually created by other Shell folder objects. To retrieve a folder's <b>IShellFolder</b> interface, you typically start by calling <a href="https://msdn.microsoft.com/121cbd41-d512-4f33-b89c-d0dd9933df87">SHGetDesktopFolder</a>. This function returns a pointer to the desktop's <b>IShellFolder</b> interface. You can then use its methods to retrieve an <b>IShellFolder</b> interface for a particular namespace folder.

<div class="alert"><b>Note</b>  <b>IShellFolder</b> methods only accept PIDLs that are relative to the folder. Some <b>IShellFolder</b> methods, such as <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">IShellFolder::GetAttributesOf</a>, only accept single-level PIDLs. In other words, the PIDL must contain only a single <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure, plus the terminating <b>NULL</b>. When you enumerate the contents of a folder with <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a>, you will receive PIDLs of this form. Other methods, such as <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">IShellFolder::CompareIDs</a>, accept multi-level PIDLs. These PIDLs can have multiple <b>SHITEMID</b> structures and identify objects one or more levels below the parent folder. Check the reference to be sure what type of PIDL can be accepted by a particular method.</div>
<div> </div>
<h3><a id="Examples"></a><a id="examples"></a><a id="EXAMPLES"></a>Examples</h3>
An example implementation of <b>IShellFolder</b> can be seen in the <a href="https://msdn.microsoft.com/B1B20AF8-3DDE-467b-A49E-A77849CF9F1B">Explorer Data Provider Sample</a> sample. The use of various <b>IShellFolder</b> methods can be found in several samples, including <a href="https://msdn.microsoft.com/A15F6C84-0B6C-493c-8E78-1FD3E08C59D8">File Operations Sample</a>.



