---
UID: NS:shlobj_core.SHARDAPPIDINFOLINK
title: SHARDAPPIDINFOLINK (shlobj_core.h)
description: Contains data used by SHAddToRecentDocs to identify both an item, in this case through an IShellLink, and the process that it is associated with.
helpviewer_keywords: ["SHARDAPPIDINFOLINK","SHARDAPPIDINFOLINK structure [Windows Shell]","_shell_SHARDAPPIDINFOLINK","shell.SHARDAPPIDINFOLINK","shlobj_core/SHARDAPPIDINFOLINK"]
old-location: shell\SHARDAPPIDINFOLINK.htm
tech.root: shell
ms.assetid: 01613dc9-4516-4995-bd31-feee2eb650b2
ms.date: 12/05/2018
ms.keywords: SHARDAPPIDINFOLINK, SHARDAPPIDINFOLINK structure [Windows Shell], _shell_SHARDAPPIDINFOLINK, shell.SHARDAPPIDINFOLINK, shlobj_core/SHARDAPPIDINFOLINK
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHARDAPPIDINFOLINK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHARDAPPIDINFOLINK
 - shlobj_core/SHARDAPPIDINFOLINK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHARDAPPIDINFOLINK
---

# SHARDAPPIDINFOLINK structure


## -description

Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> to identify both an item, in this case through an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>, and the process that it is associated with.

## -struct-fields

### -field psl

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> instance that, when launched, opens the item. The shortcut is not added by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> to the user's <b>Recent</b> folder (<a href="/windows/desktop/shell/csidl">CSIDL_RECENT</a>, <a href="/windows/desktop/shell/knownfolderid">FOLDERID_Recent</a>), but it is added to the <b>Recent</b> category in the specified application's Jump List.

### -field pszAppID

Type: <b>PCWSTR</b>

The application-defined AppUserModelID associated with the item.

## -remarks

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> instance pointed to by <b>psl</b> must provide the following:

                

<ul>
<li>Either a pointer to an item identifier list (PIDL) (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist">IShellLink::SetIDList</a>) or the target path (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath">IShellLink::SetPath</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setrelativepath">IShellLink::SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments">IShellLink::SetArguments</a>)</li>
<li>Icon location  (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation">IShellLink::SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="/windows/desktop/properties/props-system-title">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription">IShellLink::SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo">SHARDAPPIDINFO</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist">SHARDAPPIDINFOIDLIST</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>