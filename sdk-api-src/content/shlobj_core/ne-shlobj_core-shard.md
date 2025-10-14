---
UID: NE:shlobj_core.SHARD
title: SHARD (shlobj_core.h)
description: Indicates the interpretation of the data passed by SHAddToRecentDocs in its pv parameter to identify the item whose usage statistics are being tracked.
helpviewer_keywords: ["SHARD","SHARD enumeration [Windows Shell]","SHARD_APPIDINFO","SHARD_APPIDINFOIDLIST","SHARD_APPIDINFOLINK","SHARD_LINK","SHARD_PATHA","SHARD_PATHW","SHARD_PIDL","SHARD_SHELLITEM","_shell_SHARD","shell.SHARD","shlobj_core/SHARD","shlobj_core/SHARD_APPIDINFO","shlobj_core/SHARD_APPIDINFOIDLIST","shlobj_core/SHARD_APPIDINFOLINK","shlobj_core/SHARD_LINK","shlobj_core/SHARD_PATHA","shlobj_core/SHARD_PATHW","shlobj_core/SHARD_PIDL","shlobj_core/SHARD_SHELLITEM"]
old-location: shell\SHARD.htm
tech.root: shell
ms.assetid: efc9e018-41bb-44ef-9ca8-85d9e34c9899
ms.date: 12/05/2018
ms.keywords: SHARD, SHARD enumeration [Windows Shell], SHARD_APPIDINFO, SHARD_APPIDINFOIDLIST, SHARD_APPIDINFOLINK, SHARD_LINK, SHARD_PATHA, SHARD_PATHW, SHARD_PIDL, SHARD_SHELLITEM, _shell_SHARD, shell.SHARD, shlobj_core/SHARD, shlobj_core/SHARD_APPIDINFO, shlobj_core/SHARD_APPIDINFOIDLIST, shlobj_core/SHARD_APPIDINFOLINK, shlobj_core/SHARD_LINK, shlobj_core/SHARD_PATHA, shlobj_core/SHARD_PATHW, shlobj_core/SHARD_PIDL, shlobj_core/SHARD_SHELLITEM
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP, Windows 7 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHARD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHARD
 - shlobj_core/SHARD
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
 - SHARD
---

# SHARD enumeration


## -description

Indicates the interpretation of the data passed by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> in its <i>pv</i> parameter to identify the item whose usage statistics are being tracked.

## -enum-fields

### -field SHARD_PIDL

The <i>pv</i> parameter points to a PIDL that identifies the document's file object. PIDLs that identify non-file objects are not accepted.

### -field SHARD_PATHA

The <i>pv</i> parameter points to a null-terminated ANSI string with the path and file name of the object.

### -field SHARD_PATHW

The <i>pv</i> parameter points to a null-terminated Unicode string with the path and file name of the object.

### -field SHARD_APPIDINFO

<b>Windows 7 and later</b>. The <i>pv</i> parameter points to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo">SHARDAPPIDINFO</a> structure that pairs an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that identifies the item with an AppUserModelID that associates it with a particular process or application.

### -field SHARD_APPIDINFOIDLIST

<b>Windows 7 and later</b>. The <i>pv</i> parameter points to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist">SHARDAPPIDINFOIDLIST</a> structure that pairs an absolute PIDL that identifies the item with an AppUserModelID that associates it with a particular process or application.

### -field SHARD_LINK

<b>Windows 7 and later</b>. The <i>pv</i> parameter is an interface pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> object.

### -field SHARD_APPIDINFOLINK

<b>Windows 7 and later</b>. The <i>pv</i> parameter points to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink">SHARDAPPIDINFOLINK</a> structure that pairs an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> that identifies the item with an AppUserModelID that associates it with a particular process or application.

### -field SHARD_SHELLITEM

<b>Windows 7 and later</b>. The <i>pv</i> parameter is an interface pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object.

## -remarks

Before Windows 7, SHARD_PIDL, SHARD_PATHA, and SHARD_PATHW were defined as individual constants, not as enumeration members.

When providing an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> through either <b>SHARD_LINK</b> or <b>SHARD_APPIDINFOLINK</b>, the <b>IShellLink</b> instance must provide the following:

                

<ul>
<li>Either a PIDL (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist">IShellLink::SetIDList</a>) or the target path (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath">IShellLink::SetPath</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setrelativepath">IShellLink::SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments">IShellLink::SetArguments</a>)</li>
<li>Icon location  (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation">IShellLink::SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="/windows/desktop/properties/props-system-title">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription">IShellLink::SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>

