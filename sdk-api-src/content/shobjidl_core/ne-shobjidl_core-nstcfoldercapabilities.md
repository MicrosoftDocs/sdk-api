---
UID: NE:shobjidl_core.NSTCFOLDERCAPABILITIES
title: NSTCFOLDERCAPABILITIES (shobjidl_core.h)
description: Specifies the state of a tree item. These values are used by methods of the INameSpaceTreeControlFolderCapabilities interface.
helpviewer_keywords: ["NSTCFC_DELAY_REGISTER_NOTIFY","NSTCFC_NONE","NSTCFC_PINNEDITEMFILTERING","NSTCFOLDERCAPABILITIES","NSTCFOLDERCAPABILITIES enumeration [Windows Shell]","_shell_NSTCFOLDERCAPABILITIES","shell.NSTCFOLDERCAPABILITIES","shobjidl_core/NSTCFC_DELAY_REGISTER_NOTIFY","shobjidl_core/NSTCFC_NONE","shobjidl_core/NSTCFC_PINNEDITEMFILTERING","shobjidl_core/NSTCFOLDERCAPABILITIES"]
old-location: shell\NSTCFOLDERCAPABILITIES.htm
tech.root: shell
ms.assetid: a5282277-85f5-494e-b994-efbf1116b519
ms.date: 12/05/2018
ms.keywords: NSTCFC_DELAY_REGISTER_NOTIFY, NSTCFC_NONE, NSTCFC_PINNEDITEMFILTERING, NSTCFOLDERCAPABILITIES, NSTCFOLDERCAPABILITIES enumeration [Windows Shell], _shell_NSTCFOLDERCAPABILITIES, shell.NSTCFOLDERCAPABILITIES, shobjidl_core/NSTCFC_DELAY_REGISTER_NOTIFY, shobjidl_core/NSTCFC_NONE, shobjidl_core/NSTCFC_PINNEDITEMFILTERING, shobjidl_core/NSTCFOLDERCAPABILITIES
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
targetos: Windows
req.typenames: NSTCFOLDERCAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NSTCFOLDERCAPABILITIES
 - shobjidl_core/NSTCFOLDERCAPABILITIES
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
 - NSTCFOLDERCAPABILITIES
---

# NSTCFOLDERCAPABILITIES enumeration


## -description

Specifies the state of a tree item. These values are used by methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities">INameSpaceTreeControlFolderCapabilities</a> interface.

## -enum-fields

### -field NSTCFC_NONE:0

The property does not exist. Filtering is not supported.

### -field NSTCFC_PINNEDITEMFILTERING:0x1

Property exists. Supports filtering based on the value specified in <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System.IsPinnedToNameSpaceTree</a>.

### -field NSTCFC_DELAY_REGISTER_NOTIFY:0x2

Delays registration for change notifications until the tree is expanded in the navigation pane.

## -remarks

The <b>NSTCFOLDERCAPABILITIES</b> type is defined in Shobjidl.h beginning in Windows 7.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrolfoldercapabilities-getfoldercapabilities">INameSpaceTreeControlFolderCapabilities::GetFolderCapabilities</a>
