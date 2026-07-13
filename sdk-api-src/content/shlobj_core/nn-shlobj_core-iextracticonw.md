---
UID: NN:shlobj_core.IExtractIconW
title: IExtractIconW (shlobj_core.h)
description: Exposes methods that allow a client to retrieve the icon that is associated with one of the objects in a folder. (Unicode)
helpviewer_keywords: ["IExtractIcon","IExtractIcon interface [Windows Shell]","IExtractIcon interface [Windows Shell]","described","IExtractIconA","IExtractIconW","_win32_IExtractIcon","shell.IExtractIcon","shlobj_core/IExtractIcon"]
old-location: shell\IExtractIcon.htm
tech.root: shell
ms.assetid: f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f
ms.date: 12/05/2018
ms.keywords: IExtractIcon, IExtractIcon interface [Windows Shell], IExtractIcon interface [Windows Shell],described, IExtractIconA, IExtractIconW, _win32_IExtractIcon, shell.IExtractIcon, shlobj_core/IExtractIcon
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractIconW
 - shlobj_core/IExtractIconW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractIcon
---

# IExtractIconW interface


## -description

Exposes methods that allow a client to retrieve the icon that is associated with one of the objects in a folder.

## -inheritance

The <b>IExtractIcon</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtractIcon</b> also has these types of members:

## -remarks

There are two ways to retrieve an object's icon. The simplest way is to call <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a>. However, this approach is inflexible and may be slow. A more flexible and efficient way to retrieve an item's icon is to use <b>IExtractIcon</b>. The Shell uses <b>IExtractIcon</b> to retrieve icons when it displays the contents of a folder. To use <b>IExtractIcon</b> to retrieve an object's icon, do the following:

				

<ol>
<li>Get a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface of the folder that contains the object.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> with the pointer to an item identifier list (PIDL) of the object and the interface ID of <b>IExtractIcon</b> (IID_IExtractIcon). The folder creates an object to handle the icon extraction, and returns the object's <b>IExtractIcon</b> interface pointer.</li>
<li>Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> to retrieve the icon's location.</li>
<li>Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-extract">IExtractIcon::Extract</a> to retrieve the icon's handle.</li>
</ol>
It may also be possible to extract icons asynchronously on a background thread. This approach is useful when extraction is a time-consuming operation. For details, see <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>.


<a href="/windows/desktop/shell/nse-works">Namespace extensions</a> implement <b>IExtractIcon</b> to provide icons for their objects. A client obtains an <b>IExtractIcon</b> interface pointer for an object in a folder by calling the folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> method. The <b>IShellFolder::GetUIObjectOf</b> implementation must create an object to handle the icon extraction and return a pointer to the object's <b>IExtractIcon</b> interface.


<a href="/windows/desktop/shell/how-to-create-icon-handlers">Icon handlers</a> also implement <b>IExtractIcon</b>. An icon handler is a type of Shell extension handler that allows you to dynamically assign icons to the members of a <a href="/windows/desktop/shell/fa-file-types">file type</a>.

Call this interface if your application needs a more flexible way to retrieve an object's icon than <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a>.




> [!NOTE]
> The shlobj_core.h header defines IExtractIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
