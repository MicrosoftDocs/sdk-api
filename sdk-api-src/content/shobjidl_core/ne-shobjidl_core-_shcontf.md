---
UID: NE:shobjidl_core._SHCONTF
title: _SHCONTF (shobjidl_core.h)
description: Determines the types of items included in an enumeration. These values are used with the IShellFolder::EnumObjects method.
helpviewer_keywords: ["SHCONTF","SHCONTF enumeration [Windows Shell]","SHCONTF_CHECKING_FOR_CHILDREN","SHCONTF_ENABLE_ASYNC","SHCONTF_FASTITEMS","SHCONTF_FLATLIST","SHCONTF_FOLDERS","SHCONTF_INCLUDEHIDDEN","SHCONTF_INCLUDESUPERHIDDEN","SHCONTF_INIT_ON_FIRST_NEXT","SHCONTF_NAVIGATION_ENUM","SHCONTF_NETPRINTERSRCH","SHCONTF_NONFOLDERS","SHCONTF_SHAREABLE","SHCONTF_STORAGE","_SHCONTF","_win32_SHCONTF","shell.SHCONTF","shobjidl_core/SHCONTF","shobjidl_core/SHCONTF_CHECKING_FOR_CHILDREN","shobjidl_core/SHCONTF_ENABLE_ASYNC","shobjidl_core/SHCONTF_FASTITEMS","shobjidl_core/SHCONTF_FLATLIST","shobjidl_core/SHCONTF_FOLDERS","shobjidl_core/SHCONTF_INCLUDEHIDDEN","shobjidl_core/SHCONTF_INCLUDESUPERHIDDEN","shobjidl_core/SHCONTF_INIT_ON_FIRST_NEXT","shobjidl_core/SHCONTF_NAVIGATION_ENUM","shobjidl_core/SHCONTF_NETPRINTERSRCH","shobjidl_core/SHCONTF_NONFOLDERS","shobjidl_core/SHCONTF_SHAREABLE","shobjidl_core/SHCONTF_STORAGE"]
old-location: shell\SHCONTF.htm
tech.root: shell
ms.assetid: a46845bf-ade6-4366-8a73-6dc960fd7722
ms.date: 12/05/2018
ms.keywords: SHCONTF, SHCONTF enumeration [Windows Shell], SHCONTF_CHECKING_FOR_CHILDREN, SHCONTF_ENABLE_ASYNC, SHCONTF_FASTITEMS, SHCONTF_FLATLIST, SHCONTF_FOLDERS, SHCONTF_INCLUDEHIDDEN, SHCONTF_INCLUDESUPERHIDDEN, SHCONTF_INIT_ON_FIRST_NEXT, SHCONTF_NAVIGATION_ENUM, SHCONTF_NETPRINTERSRCH, SHCONTF_NONFOLDERS, SHCONTF_SHAREABLE, SHCONTF_STORAGE, _SHCONTF, _win32_SHCONTF, shell.SHCONTF, shobjidl_core/SHCONTF, shobjidl_core/SHCONTF_CHECKING_FOR_CHILDREN, shobjidl_core/SHCONTF_ENABLE_ASYNC, shobjidl_core/SHCONTF_FASTITEMS, shobjidl_core/SHCONTF_FLATLIST, shobjidl_core/SHCONTF_FOLDERS, shobjidl_core/SHCONTF_INCLUDEHIDDEN, shobjidl_core/SHCONTF_INCLUDESUPERHIDDEN, shobjidl_core/SHCONTF_INIT_ON_FIRST_NEXT, shobjidl_core/SHCONTF_NAVIGATION_ENUM, shobjidl_core/SHCONTF_NETPRINTERSRCH, shobjidl_core/SHCONTF_NONFOLDERS, shobjidl_core/SHCONTF_SHAREABLE, shobjidl_core/SHCONTF_STORAGE
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHCONTF
 - shobjidl_core/_SHCONTF
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
 - SHCONTF
---

# _SHCONTF enumeration


## -description

Determines the types of items included in an enumeration. These values are used with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> method.

## -enum-fields

### -field SHCONTF_CHECKING_FOR_CHILDREN:0x10

0x00010. <b>Windows 7 and later</b>. The calling application is checking for the existence of child items in the folder.

### -field SHCONTF_FOLDERS:0x20

0x00020. Include items that are folders in the enumeration.

### -field SHCONTF_NONFOLDERS:0x40

0x00040. Include items that are not folders in the enumeration.

### -field SHCONTF_INCLUDEHIDDEN:0x80

0x00080. Include hidden items in the enumeration. This does not include hidden system items. (To include hidden system items, use SHCONTF_INCLUDESUPERHIDDEN.)

### -field SHCONTF_INIT_ON_FIRST_NEXT:0x100

0x00100. No longer used; always assumed. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> can return without validating the enumeration object. Validation can be postponed until the first call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next">IEnumIDList::Next</a>. Use this flag when a user interface might be displayed prior to the first <b>IEnumIDList::Next</b> call. For a user interface to be presented, <i>hwnd</i> must be set to a valid window handle.

### -field SHCONTF_NETPRINTERSRCH:0x200

0x00200. The calling application is looking for printer objects.

### -field SHCONTF_SHAREABLE:0x400

0x00400. The calling application is looking for resources that can be shared.

### -field SHCONTF_STORAGE:0x800

0x00800. Include items with accessible storage and their ancestors, including hidden items.

### -field SHCONTF_NAVIGATION_ENUM:0x1000

0x01000. <b>Windows 7 and later</b>. Child folders should provide a navigation enumeration.

### -field SHCONTF_FASTITEMS:0x2000

0x02000. <b>Windows Vista and later</b>. The calling application is looking for resources that can be enumerated quickly.

### -field SHCONTF_FLATLIST:0x4000

0x04000. <b>Windows Vista and later</b>. Enumerate items as a simple list even if the folder itself is not structured in that way.

### -field SHCONTF_ENABLE_ASYNC:0x8000

0x08000. <b>Windows Vista and later</b>. The calling application is monitoring for change notifications. This means that the enumerator does not have to return all results. Items can be reported through change notifications.

### -field SHCONTF_INCLUDESUPERHIDDEN:0x10000

0x10000. <b>Windows 7 and later</b>. Include hidden system items in the enumeration. This value does not include hidden non-system items. (To include hidden non-system items, use SHCONTF_INCLUDEHIDDEN.)

## -remarks

By setting the <b><b>SHCONTF_INIT_ON_FIRST_NEXT</b></b> flag, the calling application suggests that the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> method can expedite the enumeration process by returning an uninitialized enumeration object. Initialization can be deferred until the enumeration process starts. If initializing the enumeration object is a lengthy process, the method implementation should immediately return an uninitialized object. Defer initialization until the first time the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next">IEnumIDList::Next</a> method is called. If initialization requires user input, the method implementation should use <i>hwnd</i> as the parent window for the user interface. For an explanation of what to do when <i>hwnd</i> is set to <b>NULL</b>, see the <b>IShellFolder::EnumObjects</b> reference.

<div class="alert"><b>Note</b>  The name of this enumeration was changed to <b>SHCONTF</b> in Windows Vista. Earlier, it was named <b>SHCONTF</b>. The name <b>SHCONTF</b> is still defined through a typedef statement, however, so it can continue to be used by legacy code.</div>
<div> </div>
