---
UID: NE:shobjidl_core._NSTCITEMSTATE
title: _NSTCITEMSTATE (shobjidl_core.h)
description: Specifies the state of a tree item. These values are used by methods of the INameSpaceTreeControl interface.
helpviewer_keywords: ["NSTCIS_BOLD","NSTCIS_DISABLED","NSTCIS_EXPANDED","NSTCIS_NONE","NSTCIS_SELECTED","NSTCIS_SELECTEDNOEXPAND","NSTCITEMSTATE","NSTCITEMSTATE enumeration [Windows Shell]","_NSTCITEMSTATE","_shell_NSTCITEMSTATE","shell.NSTCITEMSTATE","shobjidl_core/NSTCIS_BOLD","shobjidl_core/NSTCIS_DISABLED","shobjidl_core/NSTCIS_EXPANDED","shobjidl_core/NSTCIS_NONE","shobjidl_core/NSTCIS_SELECTED","shobjidl_core/NSTCIS_SELECTEDNOEXPAND","shobjidl_core/NSTCITEMSTATE"]
old-location: shell\NSTCITEMSTATE.htm
tech.root: shell
ms.assetid: 1f3fd526-c044-41ff-9e05-c6d91d386b42
ms.date: 12/05/2018
ms.keywords: NSTCIS_BOLD, NSTCIS_DISABLED, NSTCIS_EXPANDED, NSTCIS_NONE, NSTCIS_SELECTED, NSTCIS_SELECTEDNOEXPAND, NSTCITEMSTATE, NSTCITEMSTATE enumeration [Windows Shell], _NSTCITEMSTATE, _shell_NSTCITEMSTATE, shell.NSTCITEMSTATE, shobjidl_core/NSTCIS_BOLD, shobjidl_core/NSTCIS_DISABLED, shobjidl_core/NSTCIS_EXPANDED, shobjidl_core/NSTCIS_NONE, shobjidl_core/NSTCIS_SELECTED, shobjidl_core/NSTCIS_SELECTEDNOEXPAND, shobjidl_core/NSTCITEMSTATE
f1_keywords:
- shobjidl_core/NSTCITEMSTATE
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- shobjidl_core.h
api_name:
- NSTCITEMSTATE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _NSTCITEMSTATE enumeration


## -description


Specifies the state of a tree item. These values are used by methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> interface.


## -enum-fields




### -field NSTCIS_NONE

The item has default state; it is not selected, expanded, bolded or disabled.


### -field NSTCIS_SELECTED

The item is selected.


### -field NSTCIS_EXPANDED

The item is expanded.


### -field NSTCIS_BOLD

The item is bold.


### -field NSTCIS_DISABLED

The item is disabled.


### -field NSTCIS_SELECTEDNOEXPAND

<b>Windows 7 and later</b>. The item is selected, but not expanded.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getitemstate">INameSpaceTreeControl::GetItemState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-setitemstate">INameSpaceTreeControl::SetItemState</a>
 

 

