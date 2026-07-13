---
UID: NE:shobjidl_core.FOLDER_ENUM_MODE
title: FOLDER_ENUM_MODE (shobjidl_core.h)
description: Used by IObjectWithFolderEnumMode::GetMode and IObjectWithFolderEnumMode::SetMode methods to get and set the display modes for the folders.
helpviewer_keywords: ["FEM_NAVIGATION","FEM_VIEWRESULT","FOLDER_ENUM_MODE","FOLDER_ENUM_MODE enumeration [Windows Shell]","_shell_FOLDER_ENUM_MODE","shell.FOLDER_ENUM_MODE","shobjidl_core/FEM_NAVIGATION","shobjidl_core/FEM_VIEWRESULT","shobjidl_core/FOLDER_ENUM_MODE"]
old-location: shell\FOLDER_ENUM_MODE.htm
tech.root: shell
ms.assetid: ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a
ms.date: 12/05/2018
ms.keywords: FEM_NAVIGATION, FEM_VIEWRESULT, FOLDER_ENUM_MODE, FOLDER_ENUM_MODE enumeration [Windows Shell], _shell_FOLDER_ENUM_MODE, shell.FOLDER_ENUM_MODE, shobjidl_core/FEM_NAVIGATION, shobjidl_core/FEM_VIEWRESULT, shobjidl_core/FOLDER_ENUM_MODE
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
req.typenames: FOLDER_ENUM_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FOLDER_ENUM_MODE
 - shobjidl_core/FOLDER_ENUM_MODE
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
 - FOLDER_ENUM_MODE
---

# FOLDER_ENUM_MODE enumeration


## -description

Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode">IObjectWithFolderEnumMode::GetMode</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode">IObjectWithFolderEnumMode::SetMode</a> methods to get and set the display modes for the folders.

## -enum-fields

### -field FEM_VIEWRESULT:0

 Display mode to view the contents of a folder.

### -field FEM_NAVIGATION:1

 Display mode to view the contents of the folders in the navigation pane.

## -remarks

If an item does not support the enumeration mode value (because it is not a folder or it does not provide the enumeration mode) then it is created in the default enumeration mode.
