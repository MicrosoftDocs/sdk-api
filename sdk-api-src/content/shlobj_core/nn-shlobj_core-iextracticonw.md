---
UID: NN:shlobj_core.IExtractIconW
title: IExtractIconW (shlobj_core.h)
author: windows-sdk-content
description: Exposes methods that allow a client to retrieve the icon that is associated with one of the objects in a folder.
old-location: shell\IExtractIcon.htm
tech.root: shell
ms.assetid: f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExtractIcon, IExtractIcon interface [Windows Shell], IExtractIcon interface [Windows Shell],described, IExtractIconA, IExtractIconW, _win32_IExtractIcon, shell.IExtractIcon, shlobj_core/IExtractIcon
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IExtractIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExtractIconW interface


## -description


Exposes methods that allow a client to retrieve the icon that is associated with one of the objects in a folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtractIcon</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExtractIcon</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtractIcon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ce54876-e4f8-4f9a-8e1c-ec1db691f020">Extract</a>
</td>
<td align="left" width="63%">
Extracts an icon image from the specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">GetIconLocation</a>
</td>
<td align="left" width="63%">
Gets the location and index of an icon.

</td>
</tr>
</table> 


## -remarks



There are two ways to retrieve an object's icon. The simplest way is to call <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a>. However, this approach is inflexible and may be slow. A more flexible and efficient way to retrieve an item's icon is to use <b>IExtractIcon</b>. The Shell uses <b>IExtractIcon</b> to retrieve icons when it displays the contents of a folder. To use <b>IExtractIcon</b> to retrieve an object's icon, do the following:

				

<ol>
<li>Get a pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface of the folder that contains the object.</li>
<li>Call <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> with the pointer to an item identifier list (PIDL) of the object and the interface ID of <b>IExtractIcon</b> (IID_IExtractIcon). The folder creates an object to handle the icon extraction, and returns the object's <b>IExtractIcon</b> interface pointer.</li>
<li>Call <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> to retrieve the icon's location.</li>
<li>Call <a href="https://msdn.microsoft.com/3ce54876-e4f8-4f9a-8e1c-ec1db691f020">IExtractIcon::Extract</a> to retrieve the icon's handle.</li>
</ol>
It may also be possible to extract icons asynchronously on a background thread. This approach is useful when extraction is a time-consuming operation. For details, see <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>.


<a href="https://msdn.microsoft.com/cc387338-15fa-4350-b039-61a0f1c5030a">Namespace extensions</a> implement <b>IExtractIcon</b> to provide icons for their objects. A client obtains an <b>IExtractIcon</b> interface pointer for an object in a folder by calling the folder's <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> method. The <b>IShellFolder::GetUIObjectOf</b> implementation must create an object to handle the icon extraction and return a pointer to the object's <b>IExtractIcon</b> interface.


<a href="https://msdn.microsoft.com/23ed3a21-cf62-4440-b983-fae23aa56890">Icon handlers</a> also implement <b>IExtractIcon</b>. An icon handler is a type of Shell extension handler that allows you to dynamically assign icons to the members of a <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">file type</a>.

Call this interface if your application needs a more flexible way to retrieve an object's icon than <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a>.



