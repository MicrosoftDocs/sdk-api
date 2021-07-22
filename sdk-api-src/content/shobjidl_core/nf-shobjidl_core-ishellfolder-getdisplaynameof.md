---
UID: NF:shobjidl_core.IShellFolder.GetDisplayNameOf
title: IShellFolder::GetDisplayNameOf (shobjidl_core.h)
description: Retrieves the display name for the specified file object or subfolder.
helpviewer_keywords: ["GetDisplayNameOf","GetDisplayNameOf method [Windows Shell]","GetDisplayNameOf method [Windows Shell]","IShellFolder interface","GetDisplayNameOf method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","GetDisplayNameOf method","IShellFolder.GetDisplayNameOf","IShellFolder2 interface [Windows Shell]","GetDisplayNameOf method","IShellFolder2::GetDisplayNameOf","IShellFolder::GetDisplayNameOf","_win32_IShellFolder_GetDisplayNameOf","shell.IShellFolder_GetDisplayNameOf","shobjidl_core/IShellFolder2::GetDisplayNameOf","shobjidl_core/IShellFolder::GetDisplayNameOf"]
old-location: shell\IShellFolder_GetDisplayNameOf.htm
tech.root: shell
ms.assetid: 2164bbe6-e030-4a64-85db-9ee1cd3c136d
ms.date: 12/05/2018
ms.keywords: GetDisplayNameOf, GetDisplayNameOf method [Windows Shell], GetDisplayNameOf method [Windows Shell],IShellFolder interface, GetDisplayNameOf method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],GetDisplayNameOf method, IShellFolder.GetDisplayNameOf, IShellFolder2 interface [Windows Shell],GetDisplayNameOf method, IShellFolder2::GetDisplayNameOf, IShellFolder::GetDisplayNameOf, _win32_IShellFolder_GetDisplayNameOf, shell.IShellFolder_GetDisplayNameOf, shobjidl_core/IShellFolder2::GetDisplayNameOf, shobjidl_core/IShellFolder::GetDisplayNameOf
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder::GetDisplayNameOf
 - shobjidl_core/IShellFolder::GetDisplayNameOf
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
 - IShellFolder.GetDisplayNameOf
 - IShellFolder2.GetDisplayNameOf
---

# IShellFolder::GetDisplayNameOf


## -description

Retrieves the display name for the specified file object or subfolder.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL that uniquely identifies the file object or subfolder relative to the parent folder.

### -param uFlags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDNF</a></b>

Flags used to request the type of display name to return. For a list of possible values, see the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDNF</a> enumerated type.

### -param pName [out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

When this method returns, contains a pointer to a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure in which to return the display name. The type of name returned in this structure can be the requested type, but the Shell folder might return a different type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is the caller's responsibility to free resources allocated by this function.

Normally, <i>pidl</i> can refer only to items contained by the parent folder. The PIDL must be single-level and contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero. If you want to retrieve the display name of an item that is deeper than one level away from the parent folder, use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent">SHBindToParent</a> to bind with the item's immediate parent folder and then pass the item's single-level PIDL to <b>IShellFolder::GetDisplayNameOf</b>.

Also, if the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_FORPARSING</a> flag is set in <i>uFlags</i> and the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_INFOLDER</a> flag is not set, <i>pidl</i> can refer to an object at any level below the parent folder in the namespace hierarchy. At one time, <i>pidl</i> could be a multilevel PIDL, relative to the parent folder, and could contain multiple <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structures. However, this is no longer supported and <i>pidl</i> should now refer only to a single child item.

The simplest way to retrieve the display name from the structure pointed to by <i>pName</i> is to pass it to either <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettobufa">StrRetToBuf</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a>. These functions take a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure and return the name. You can also examine the structure's <b>uType</b> member, and retrieve the name from the appropriate member.

The flags specified in <i>uFlags</i> are hints about the intended use of the name. They do not guarantee that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> will return the requested form of the name. If that form is not available, a different one might be returned. In particular, there is no guarantee that the name returned by the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_FORPARSING</a> flag will be successfully parsed by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>. There are also some combinations of flags that might cause the <b>GetDisplayNameOf</b>/<b>ParseDisplayName</b> round trip to not return the original identifier list. This occurrence is exceptional, but you should check to be sure.

<div class="alert"><b>Note</b>  The parsing name that is returned when <i>uFlags</i> has the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_FORPARSING</a> flag set is not necessarily a normal text string. Virtual folders such as My Computer might return a string containing the folder object's GUID in the form "::{GUID}". Developers who implement <b>IShellFolder::GetDisplayNameOf</b> are encouraged to return parse names that are as close to the display names as possible, because the end user often needs to type or edit these names.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>