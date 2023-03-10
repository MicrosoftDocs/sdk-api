---
UID: NS:shobjidl_core.FOLDERSETTINGS
title: FOLDERSETTINGS (shobjidl_core.h)
description: Contains folder view information.
helpviewer_keywords: ["*LPFOLDERSETTINGS","*PFOLDERSETTINGS","FOLDERSETTINGS","FOLDERSETTINGS structure [Windows Shell]","_win32_FOLDERSETTINGS","shell.FOLDERSETTINGS","shobjidl_core/FOLDERSETTINGS"]
old-location: shell\FOLDERSETTINGS.htm
tech.root: shell
ms.assetid: be00fe39-1add-412e-b88b-4b0b1404b19d
ms.date: 12/05/2018
ms.keywords: '*LPFOLDERSETTINGS, *PFOLDERSETTINGS, FOLDERSETTINGS, FOLDERSETTINGS structure [Windows Shell], _win32_FOLDERSETTINGS, shell.FOLDERSETTINGS, shobjidl_core/FOLDERSETTINGS'
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
req.typenames: FOLDERSETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FOLDERSETTINGS
 - shobjidl_core/FOLDERSETTINGS
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
 - FOLDERSETTINGS
---

# FOLDERSETTINGS structure


## -description

Contains folder view information.

## -struct-fields

### -field ViewMode

Type: <b>UINT</b>

Folder view mode. One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode">FOLDERVIEWMODE</a> values.

### -field fFlags

Type: <b>UINT</b>

A set of flags that indicate the options for the folder. This can be zero or a combination of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a> values.

## -remarks

These settings assume a particular user interface, which the Shell's folder view has. A Shell extension can use these settings if they apply to the view implemented by the extension.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow">IShellView::CreateViewWindow</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo">IShellView::GetCurrentInfo</a>