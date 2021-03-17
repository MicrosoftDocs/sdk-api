---
UID: NS:shobjidl_core._PERSIST_FOLDER_TARGET_INFO
title: PERSIST_FOLDER_TARGET_INFO (shobjidl_core.h)
description: Specifies a folder shortcut's target folder and its attributes. This structure is used by IPersistFolder3::GetFolderTargetInfo and IPersistFolder3::InitializeEx.
helpviewer_keywords: ["CSIDL_FLAG_CREATE","CSIDL_FLAG_PFTI_TRACKTARGET","PERSIST_FOLDER_TARGET_INFO","PERSIST_FOLDER_TARGET_INFO structure [Windows Shell]","_PERSIST_FOLDER_TARGET_INFO","_win32_PERSIST_FOLDER_TARGET_INFO_str","shell.PERSIST_FOLDER_TARGET_INFO_str","shobjidl_core/PERSIST_FOLDER_TARGET_INFO"]
old-location: shell\PERSIST_FOLDER_TARGET_INFO_str.htm
tech.root: shell
ms.assetid: 74441551-c315-4203-a4f5-cd4e6c57b58b
ms.date: 12/05/2018
ms.keywords: CSIDL_FLAG_CREATE, CSIDL_FLAG_PFTI_TRACKTARGET, PERSIST_FOLDER_TARGET_INFO, PERSIST_FOLDER_TARGET_INFO structure [Windows Shell], _PERSIST_FOLDER_TARGET_INFO, _win32_PERSIST_FOLDER_TARGET_INFO_str, shell.PERSIST_FOLDER_TARGET_INFO_str, shobjidl_core/PERSIST_FOLDER_TARGET_INFO
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PERSIST_FOLDER_TARGET_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERSIST_FOLDER_TARGET_INFO
 - shobjidl_core/_PERSIST_FOLDER_TARGET_INFO
 - PERSIST_FOLDER_TARGET_INFO
 - shobjidl_core/PERSIST_FOLDER_TARGET_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - PERSIST_FOLDER_TARGET_INFO
---

# PERSIST_FOLDER_TARGET_INFO structure


## -description

Specifies a folder shortcut's target folder and its attributes. This structure is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo">IPersistFolder3::GetFolderTargetInfo</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex">IPersistFolder3::InitializeEx</a>.

## -struct-fields

### -field pidlTargetFolder

Type: <b>PIDLIST_ABSOLUTE</b>

A fully qualified PIDL of the target folder. Set <b>pidlTargetFolder</b> to <b>NULL</b> if not specified.

### -field szTargetParsingName

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string with the target folder's parsing name. Set <b>szTargetParsingName</b> to an empty string if not specified.

### -field szNetworkProvider

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string that specifies the type of network provider that will be used when binding to the target folder. The format is the same as that used by the <a href="/windows/desktop/WNet/windows-networking-wnet-">WNet API</a>. Set <b>szNetworkProvider</b> to an empty string if not specified.

### -field dwAttributes

Type: <b>DWORD</b>

A <b>DWORD</b> value that contains FILE_ATTRIBUTE_* flags as defined in Winnt.h. Set <b>dwAttributes</b> to -1 if not specified.

### -field csidl

Type: <b>int</b>

The target folder's <a href="/windows/desktop/shell/csidl">CSIDL</a> value, if it has one. Set <b>csidl</b> to -1 if the target folder does not have a CSIDL. In addition to the CSIDL value, you can also set the following two flags.



#### CSIDL_FLAG_PFTI_TRACKTARGET

Indicates that the target folder should change if the user changes the target folder's underlying CSIDL value.



#### CSIDL_FLAG_CREATE

Indicates that the target folder should be created if it does not already exist.

## -remarks

Any or all of the <b>pidlTargetFolder</b>, <b>szTargetParsingName</b>, and <b>csidl</b> members can be used to specify the target folder's location.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3">IPersistFolder3</a>