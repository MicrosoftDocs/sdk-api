---
UID: NE:shobjidl_core._SHGDNF
title: _SHGDNF (shobjidl_core.h)
description: Defines the values used with the IShellFolder::GetDisplayNameOf and IShellFolder::SetNameOf methods to specify the type of file or folder names used by those methods.
helpviewer_keywords: ["SHGDNF","SHGDNF enumeration [Windows Shell]","SHGDN_FORADDRESSBAR","SHGDN_FOREDITING","SHGDN_FORPARSING","SHGDN_INFOLDER","SHGDN_NORMAL","_SHGDNF","_win32_SHGNO","shell.SHGNO","shobjidl_core/SHGDNF","shobjidl_core/SHGDN_FORADDRESSBAR","shobjidl_core/SHGDN_FOREDITING","shobjidl_core/SHGDN_FORPARSING","shobjidl_core/SHGDN_INFOLDER","shobjidl_core/SHGDN_NORMAL"]
old-location: shell\SHGNO.htm
tech.root: shell
ms.assetid: 5d87609d-bcbf-4a4f-a97e-017ee8a9879e
ms.date: 12/05/2018
ms.keywords: SHGDNF, SHGDNF enumeration [Windows Shell], SHGDN_FORADDRESSBAR, SHGDN_FOREDITING, SHGDN_FORPARSING, SHGDN_INFOLDER, SHGDN_NORMAL, _SHGDNF, _win32_SHGNO, shell.SHGNO, shobjidl_core/SHGDNF, shobjidl_core/SHGDN_FORADDRESSBAR, shobjidl_core/SHGDN_FOREDITING, shobjidl_core/SHGDN_FORPARSING, shobjidl_core/SHGDN_INFOLDER, shobjidl_core/SHGDN_NORMAL
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 7 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHGDNF
 - shobjidl_core/_SHGDNF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHGDNF
---

# _SHGDNF enumeration


## -description

Defines the values used with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof">IShellFolder::SetNameOf</a> methods to specify the type of file or folder names used by those methods.

            
<div class="alert"><b>Note</b>  Prior to Windows 7, these values were packaged as the SHGNO enumeration.</div><div> </div>

## -enum-fields

### -field SHGDN_NORMAL:0

When not combined with another flag, return the parent-relative name that identifies the item, suitable for displaying to the user. This name often does not include extra information such as the file name extension and does not need to be unique. This name might include information that identifies the folder that contains the item. For instance, this flag could cause <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> to return the string "<b>username</b> (on <b>Machine</b>)" for a particular user's folder.

### -field SHGDN_INFOLDER:0x1

The name is relative to the folder from which the request was made. This is the name display to the user when used in the context of the folder. For example, it is used in the view and in the address bar path segment for the folder. This name should not include disambiguation information—for instance "<b>username</b>" instead of "<b>username</b> (on <i>Machine</i>)" for a particular user's folder.

Use this flag in combinations with <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_FORPARSING</a> and <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_FOREDITING</a>.

### -field SHGDN_FOREDITING:0x1000

The name is used for in-place editing when the user renames the item.

### -field SHGDN_FORADDRESSBAR:0x4000

The name is displayed in an address bar combo box.

### -field SHGDN_FORPARSING:0x8000

The name is used for parsing. That is, it can be passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> to recover the object's PIDL. The form this name takes depends on the particular object. When SHGDN_FORPARSING is used alone, the name is relative to the desktop. When combined with SHGDN_INFOLDER, the name is relative to the folder from which the request was made.

## -remarks

The <b>SHGDNF</b> type is defined in Shobjidl.h as shown here.

                


```
typedef DWORD SHGDNF;
```


This enumeration consists of two groups of values. The first group—SHGDN_NORMAL and SHGDN_INFOLDER—specifies the name's type. The second group—SHGDN_FOREDITING, SHGDN_FORADDRESSBAR, and SHGDN_FORPARSING—consists of modifiers to the first group that specify name retrieval options.

If SHGDN_FORPARSING is set and SHGDN_INFOLDER is not set, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> can accept a PIDL that contains more than an <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure. Otherwise, only a single-level PIDL can be passed.

<b>Note</b> While the parsing name returned by file system objects is the object's fully qualified path, virtual folders might use something quite different. For example, some virtual folders use a GUID as the parsing name and return a string of the form "::{GUID}". To check whether the object is part of the file system, call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a> and see if the <b>SFGAO_FILESYSTEM</b> flag is set. Developers who implement <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> are encouraged to return parse names that are as close to the display names as possible, because the end user often needs to type or edit these names.

The numeric value of SHGDN_NORMAL is zero, so you cannot test for the presence of this bit. Consider SHGDN_NORMAL a default setting that is used if no other flag in that group is set.

<b>Example</b>

The following tables illustrate an example of possible return values for five different flag options and three different item types.

These are the flag options.

<table class="clsStd">
<tr>
<th>Number</th>
<th>Flags</th>
<th>Description</th>
</tr>
<tr>
<td>1</td>
<td>SHGDN_FORPARSING</td>
<td>Returns the fully qualified parsing name.</td>
</tr>
<tr>
<td>2</td>
<td>SHGDN_INFOLDER | SHGDN_FORPARSING</td>
<td>Returns the parsing name relative to the parent folder.</td>
</tr>
<tr>
<td>3</td>
<td>SHGDN_INFOLDER | SHGDN_FOREDITING</td>
<td>Returns the editing name relative to the parent folder.</td>
</tr>
<tr>
<td>4</td>
<td>SHGDN_INFOLDER</td>
<td>Returns the display name relative to the parent folder.</td>
</tr>
<tr>
<td>5</td>
<td>SHGDN_NORMAL</td>
<td>Returns the display name relative to the desktop and not to a specific folder.</td>
</tr>
</table>
 

These are the sample item types.

<table class="clsStd">
<tr>
<th>Letter</th>
<th>Description</th>
</tr>
<tr>
<td>A</td>
<td>The C: drive on the local computer, whose volume label is C_DRIVE.</td>
</tr>
<tr>
<td>B</td>
<td>A printer named Laser on a computer called Mailroom.</td>
</tr>
<tr>
<td>C</td>
<td>The file C:\Directory\File.txt (when file-name extensions are hidden).</td>
</tr>
</table>
 

The following table describes the display names as they would be returned.

<table class="clsStd">
<tr>
<th></th>
<th>A</th>
<th>B</th>
<th>C</th>
</tr>
<tr>
<th>1</th>
<td>C:\</td>
<td>\\Mailroom\Laser</td>
<td>C:\Directory\File.txt</td>
</tr>
<tr>
<th>2</th>
<td>C:\</td>
<td>Laser</td>
<td>File.txt</td>
</tr>
<tr>
<th>3</th>
<td>C_DRIVE</td>
<td>Laser</td>
<td>File</td>
</tr>
<tr>
<th>4</th>
<td>C_DRIVE (C:)</td>
<td>Laser</td>
<td>File</td>
</tr>
<tr>
<th>5</th>
<td>C_DRIVE (C:)</td>
<td>Laser on Mailroom</td>
<td>File</td>
</tr>
</table>
 

<b>Remarks on examples</b>

<ul>
<li>A3: The C: drive presents its volume name for editing, rather than the entire string "C_DRIVE (C:)".</li>
<li>B1-B5: The display name of the remote printer changes depending on whether it is being shown relative to its parent. When shown relative to its parent, it needs only its printer name, but when shown outside its parent, it shows both its printer name and its computer name.</li>
<li>C3: File.txt presents only its base name for editing instead of its full name.</li>
</ul>
For further discussion of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface, see <a href="/windows/desktop/shell/folder-info">Getting Information About the Contents of a Folder</a>.
