---
UID: NE:shobjidl_core.KF_CATEGORY
title: KF_CATEGORY (shobjidl_core.h)
description: Value that represent a category by which a folder registered with the Known Folder system can be classified.
helpviewer_keywords: ["KF_CATEGORY","KF_CATEGORY enumeration [Windows Shell]","KF_CATEGORY_COMMON","KF_CATEGORY_FIXED","KF_CATEGORY_PERUSER","KF_CATEGORY_VIRTUAL","_shell_KF_CATEGORY","shell.KF_CATEGORY","shobjidl_core/KF_CATEGORY","shobjidl_core/KF_CATEGORY_COMMON","shobjidl_core/KF_CATEGORY_FIXED","shobjidl_core/KF_CATEGORY_PERUSER","shobjidl_core/KF_CATEGORY_VIRTUAL"]
old-location: shell\KF_CATEGORY.htm
tech.root: shell
ms.assetid: 2ca0d3e2-bb4c-4a28-90d6-fe2852373b88
ms.date: 12/05/2018
ms.keywords: KF_CATEGORY, KF_CATEGORY enumeration [Windows Shell], KF_CATEGORY_COMMON, KF_CATEGORY_FIXED, KF_CATEGORY_PERUSER, KF_CATEGORY_VIRTUAL, _shell_KF_CATEGORY, shell.KF_CATEGORY, shobjidl_core/KF_CATEGORY, shobjidl_core/KF_CATEGORY_COMMON, shobjidl_core/KF_CATEGORY_FIXED, shobjidl_core/KF_CATEGORY_PERUSER, shobjidl_core/KF_CATEGORY_VIRTUAL
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: KF_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KF_CATEGORY
 - shobjidl_core/KF_CATEGORY
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
 - KF_CATEGORY
---

# KF_CATEGORY enumeration


## -description

Value that represent a category by which a folder registered with the Known Folder system can be classified.

## -enum-fields

### -field KF_CATEGORY_VIRTUAL:1

Virtual folders are not part of the file system, which is to say that they have no path. For example, <b>Control Panel</b> and <b>Printers</b> are virtual folders. A number of features such as folder path and redirection do not apply to this category.

### -field KF_CATEGORY_FIXED:2

Fixed file system folders are not managed by the Shell and are usually given a permanent path when the system is installed. For example, the <b>Windows</b> and <b>Program Files</b> folders are fixed folders. A number of features such as redirection do not apply to this category.

### -field KF_CATEGORY_COMMON:3

Common folders are those file system folders used for sharing data and settings, accessible by all users of a system. For example, all users share a common <b>Documents</b> folder as well as their per-user <b>Documents</b> folder.

### -field KF_CATEGORY_PERUSER:4

Per-user folders are those stored under each user's profile and accessible only by that user. For example, <code>%USERPROFILE%\Pictures</code>. This category of folder usually supports many features including aliasing, redirection and customization. 
                
                



<div class="alert"><b>Note</b>  The user profile root folder (<a href="/windows/desktop/shell/knownfolderid">FOLDERID_Profile</a>) does not support redirection.</div>
<div> </div>

## -remarks

The <b>KF_CATEGORY</b> type is defined in Shobjidl.h as shown here.

                


```
typedef DWORD KF_CATEGORY;
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getcategory">IKnownFolder::GetCategory</a>



<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
