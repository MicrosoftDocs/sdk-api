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
f1_keywords: 
 - "shlobj_core/IExtractIcon"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtractIconW interface


## -description


Exposes methods that allow a client to retrieve the icon that is associated with one of the objects in a folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtractIcon</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtractIcon</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-extract">Extract</a>
</td>
<td align="left" width="63%">
Extracts an icon image from the specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">GetIconLocation</a>
</td>
<td align="left" width="63%">
Gets the location and index of an icon.

</td>
</tr>
</table> 


## -remarks



There are two ways to retrieve an object's icon. The simplest way is to call <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a>. However, this approach is inflexible and may be slow. A more flexible and efficient way to retrieve an item's icon is to use <b>IExtractIcon</b>. The Shell uses <b>IExtractIcon</b> to retrieve icons when it displays the contents of a folder. To use <b>IExtractIcon</b> to retrieve an object's icon, do the following:

				

<ol>
<li>Get a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface of the folder that contains the object.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> with the pointer to an item identifier list (PIDL) of the object and the interface ID of <b>IExtractIcon</b> (IID_IExtractIcon). The folder creates an object to handle the icon extraction, and returns the object's <b>IExtractIcon</b> interface pointer.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> to retrieve the icon's location.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-extract">IExtractIcon::Extract</a> to retrieve the icon's handle.</li>
</ol>
It may also be possible to extract icons asynchronously on a background thread. This approach is useful when extraction is a time-consuming operation. For details, see <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>.


<a href="https://docs.microsoft.com/windows/desktop/shell/nse-works">Namespace extensions</a> implement <b>IExtractIcon</b> to provide icons for their objects. A client obtains an <b>IExtractIcon</b> interface pointer for an object in a folder by calling the folder's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> method. The <b>IShellFolder::GetUIObjectOf</b> implementation must create an object to handle the icon extraction and return a pointer to the object's <b>IExtractIcon</b> interface.


<a href="https://docs.microsoft.com/windows/desktop/shell/how-to-create-icon-handlers">Icon handlers</a> also implement <b>IExtractIcon</b>. An icon handler is a type of Shell extension handler that allows you to dynamically assign icons to the members of a <a href="https://docs.microsoft.com/windows/desktop/shell/fa-file-types">file type</a>.

Call this interface if your application needs a more flexible way to retrieve an object's icon than <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a>.



