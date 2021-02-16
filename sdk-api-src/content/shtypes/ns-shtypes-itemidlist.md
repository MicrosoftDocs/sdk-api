---
UID: NS:shtypes._ITEMIDLIST
title: ITEMIDLIST (shtypes.h)
description: Contains a list of item identifiers.
helpviewer_keywords: ["*LPITEMIDLIST","*PIDLIST_ABSOLUTE","*PIDLIST_RELATIVE","*PITEMID_CHILD","*PUIDLIST_RELATIVE","*PUITEMID_CHILD","ITEMIDLIST","ITEMIDLIST structure [Windows Shell]","ITEMIDLIST_ABSOLUTE","ITEMIDLIST_RELATIVE","ITEMID_CHILD","_win32_ITEMIDLIST","shell.ITEMIDLIST","shtypes/ITEMIDLIST"]
old-location: shell\ITEMIDLIST.htm
tech.root: shell
ms.assetid: 60daf071-4e93-4e1c-bc38-894f706db04f
ms.date: 12/05/2018
ms.keywords: '*LPITEMIDLIST, *PIDLIST_ABSOLUTE, *PIDLIST_RELATIVE, *PITEMID_CHILD, *PUIDLIST_RELATIVE, *PUITEMID_CHILD, ITEMIDLIST, ITEMIDLIST structure [Windows Shell], ITEMIDLIST_ABSOLUTE, ITEMIDLIST_RELATIVE, ITEMID_CHILD, _win32_ITEMIDLIST, shell.ITEMIDLIST, shtypes/ITEMIDLIST'
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ITEMIDLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ITEMIDLIST
 - shtypes/_ITEMIDLIST
 - ITEMIDLIST
 - shtypes/ITEMIDLIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - ITEMIDLIST
---

# ITEMIDLIST structure


## -description

Contains a list of item identifiers.

## -struct-fields

### -field mkid

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a></b>

A list of item identifiers.

## -remarks

A pointer to this structure, called a <i>PIDL</i>, is used to identify objects in the Shell namespace.  For more information about pointers to item identifier lists (PIDLs) and item identifiers, see <a href="/windows/desktop/shell/namespace-intro">Introduction to the Shell Namespace</a>.

<h3><a id="ITEMIDLIST_Strict_Types"></a><a id="itemidlist_strict_types"></a><a id="ITEMIDLIST_STRICT_TYPES"></a>ITEMIDLIST Strict Types</h3>
As of Windows Vista, several forms of <b>ITEMIDLIST</b> are available as data types. The three main types are:

                

<ul>
<li>IDLIST_ABSOLUTE: Fully qualified <b>ITEMIDLIST</b> relative to the root of the namespace. It may be multi-level.</li>
<li>IDLIST_RELATIVE: <b>ITEMIDLIST</b> relative to a parent folder. It may be multi-level.</li>
<li>ITEMID_CHILD: Single-level <b>ITEMIDLIST</b> relative to a parent folder. It contains exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure.</li>
</ul>
These types are used if you compile your code with the symbol STRICT_TYPED_ITEMIDS before you include the Shell header files, as shown in the following example code.


```

#define STRICT_TYPED_ITEMIDS    // Better type safety for IDLists

#include <shlobj.h>             // Typical Shell header file
```


The meaning of each of these types can be altered with one or more of the following modifiers:

<ul>
<li>P: The type is a pointer.</li>
<li>C: The type is constant.</li>
<li>U: The type is unaligned. It aligns to a <b>DWORD</b> boundary in 32-bit architectures and a <b>QWORD</b> boundary in 64-bit architectures.</li>
</ul>
Some examples of these modified types are:

<ul>
<li>PIDLIST_ABSOLUTE: The <b>ITEMIDLIST</b> is absolute and has been allocated, as indicated by its being non-constant. This means that it needs to be deallocated with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> when it is no longer needed. Because it is a direct pointer to allocated memory, it is aligned.</li>
<li>PCIDLIST_ABSOLUTE: The <b>ITEMIDLIST</b> is absolute and constant. This is typically used when you are passed an absolute <b>ITEMIDLIST</b> as a parameter but do not own it, and so are not allowed to change it.</li>
<li>PCUIDLIST_ABSOLUTE: The <b>ITEMIDLIST</b> is absolute, constant and unaligned. This is rarely used. Absolute <b>ITEMIDLIST</b> are typically allocated in memory aligned to a <b>DWORD</b> boundary in 32-bit architectures and to a <b>QWORD</b> boundary in 64-bit architectures. An absolute <b>ITEMIDLIST</b> would be unaligned only if it has been byte-packed along with other data, such as in a serialization format.</li>
<li>PITEMID_CHILD: The <b>ITEMIDLIST</b> is an allocated child <b>ITEMIDLIST</b> relative to a parent folder, such as a result of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next">IEnumIDList::Next</a>. It contains exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure.</li>
<li>PCUITEMID_CHILD: The child <b>ITEMIDLIST</b> is relative, constant, and unaligned. This often occurs when you get a pointer to part of an existing PIDL. For example, if you have an absolute PIDL and call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid">ILFindLastID</a>, it returns the pointer to the last child <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> in the list. It is unaligned because the byte-packed PIDL does not ensure that its individual <b>SHITEMID</b> structures fall on byte boundaries. References to child PIDLs such as these are always constant because the memory is owned by the absolute PIDL.</li>
<li>PCITEMID_CHILD: The child <b>ITEMIDLIST</b> is constant and aligned. This is rarely used because as a child PIDL, it is usually a part of a larger PIDL, and therefore not aligned on byte boundaries.</li>
<li>PUITEMID_CHILD: The child <b>ITEMIDLIST</b> is unaligned. This is rarely used because memory for this <b>ITEMIDLIST</b> is owned by the parent PIDL, which is absolute. This means that modifications can be made only to the parent PIDL, and so the child PIDL would need to be constant.</li>
</ul>
This list is not exhaustive. Other types can also exist.