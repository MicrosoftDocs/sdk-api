---
UID: NS:shlobj_core._QCMINFO
title: QCMINFO (shlobj_core.h)
description: Contains information for merging menu items into Windows Explorer menus.
helpviewer_keywords: ["*LPQCMINFO","QCMINFO","QCMINFO structure [Windows Shell]","_QCMINFO","_win32_QCMINFO_str","shell.QCMINFO_str","shlobj_core/QCMINFO"]
old-location: shell\QCMINFO_str.htm
tech.root: shell
ms.assetid: 3f991ebb-d66c-4bdc-b9d2-2bf6bb5a269a
ms.date: 12/05/2018
ms.keywords: '*LPQCMINFO, QCMINFO, QCMINFO structure [Windows Shell], _QCMINFO, _win32_QCMINFO_str, shell.QCMINFO_str, shlobj_core/QCMINFO'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: QCMINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QCMINFO
 - shlobj_core/_QCMINFO
 - QCMINFO
 - shlobj_core/QCMINFO
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
 - QCMINFO
---

# QCMINFO structure


## -description

Contains information for merging menu items into Windows Explorer menus.

## -struct-fields

### -field hmenu

Type: <b>HMENU</b>

[in] The handle of the menu where the new commands are to be added.

### -field indexMenu

Type: <b>UINT</b>

[in] The zero-based index where the first menu item are to be inserted.

### -field idCmdFirst

Type: <b>UINT</b>

[in, out] On entry, this member contains the first available ID to be used for the context menu. On exit, it contains the last ID added plus one.

### -field idCmdLast

Type: <b>UINT</b>

[in] The maximum value for a menu item identifier. The difference between the input value of <b>idCmdFirst</b> and <b>idCmdLast</b> is the maximum number of menu items that can be added.

### -field pIdMap

Type: <b>QCMINFO_IDMAP*</b>

Not used, must be <b>NULL</b>.

## -remarks

See <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu">IContextMenu::QueryContextMenu</a> as this structure performs the same role as the parameters of that method. Note, however, that the information provided by the return value of that method is not a parallel to the information provided by the return value of an operation involving <b>QCMINFO</b>.

## -see-also

<a href="/windows/desktop/shell/registering-control-panel-items">DFM_MERGECONTEXTMENU</a>



<a href="/windows/desktop/shell/reg-middleware-apps">DFM_MERGECONTEXTMENU_BOTTOM</a>



<a href="/windows/desktop/shell/samples-aerowizards">DFM_MERGECONTEXTMENU_TOP</a>



<a href="/windows/desktop/shell/sfvm-mergemenu">SFVM_MERGEMENU</a>