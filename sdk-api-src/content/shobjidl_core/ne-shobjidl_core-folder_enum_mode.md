---
UID: NE:shobjidl_core.FOLDER_ENUM_MODE
title: FOLDER_ENUM_MODE
author: windows-sdk-content
description: Used by IObjectWithFolderEnumMode::GetMode and IObjectWithFolderEnumMode::SetMode methods to get and set the display modes for the folders.
old-location: shell\FOLDER_ENUM_MODE.htm
tech.root: shell
ms.assetid: ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: FEM_NAVIGATION, FEM_VIEWRESULT, FOLDER_ENUM_MODE, FOLDER_ENUM_MODE enumeration [Windows Shell], _shell_FOLDER_ENUM_MODE, shell.FOLDER_ENUM_MODE, shobjidl_core/FEM_NAVIGATION, shobjidl_core/FEM_VIEWRESULT, shobjidl_core/FOLDER_ENUM_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FOLDER_ENUM_MODE
product: Windows
targetos: Windows
req.typenames: FOLDER_ENUM_MODE
req.redist: 
---

# FOLDER_ENUM_MODE enumeration


## -description


Used by <a href="https://msdn.microsoft.com/5d331255-2295-4f7b-b2d6-1238edcc15bb">IObjectWithFolderEnumMode::GetMode</a> and <a href="https://msdn.microsoft.com/7e7271ec-47a7-42bf-ab02-26cd587448bd">IObjectWithFolderEnumMode::SetMode</a> methods to get and set the display modes for the folders.


## -enum-fields




### -field FEM_VIEWRESULT

 Display mode to view the contents of a folder.


### -field FEM_NAVIGATION

 Display mode to view the contents of the folders in the navigation pane.


## -remarks



If an item does not support the enumeration mode value (because it is not a folder or it does not provide the enumeration mode) then it is created in the default enumeration mode.



