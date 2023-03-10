---
UID: NS:shlobj_core._SHChangeNotifyEntry
title: SHChangeNotifyEntry (shlobj_core.h)
description: Contains and receives information for change notifications. This structure is used with the SHChangeNotifyRegister function and the SFVM_QUERYFSNOTIFY notification.
helpviewer_keywords: ["SHChangeNotifyEntry","SHChangeNotifyEntry structure [Windows Shell]","_SHChangeNotifyEntry","_win32_SHChangeNotifyEntry","shell.SHChangeNotifyEntry","shlobj_core/SHChangeNotifyEntry"]
old-location: shell\SHChangeNotifyEntry.htm
tech.root: shell
ms.assetid: cb11435a-86f0-4b06-bfc6-e0417f2897a1
ms.date: 12/05/2018
ms.keywords: SHChangeNotifyEntry, SHChangeNotifyEntry structure [Windows Shell], _SHChangeNotifyEntry, _win32_SHChangeNotifyEntry, shell.SHChangeNotifyEntry, shlobj_core/SHChangeNotifyEntry
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
req.typenames: SHChangeNotifyEntry
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHChangeNotifyEntry
 - shlobj_core/_SHChangeNotifyEntry
 - SHChangeNotifyEntry
 - shlobj_core/SHChangeNotifyEntry
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
 - SHChangeNotifyEntry
---

# SHChangeNotifyEntry structure


## -description

Contains and receives information for change notifications. This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister">SHChangeNotifyRegister</a> function and the <a href="/windows/desktop/shell/sfvm-queryfsnotify">SFVM_QUERYFSNOTIFY</a> notification.

## -struct-fields

### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

PIDL for which to receive notifications.

### -field fRecursive

Type: <b>BOOL</b>

A flag indicating whether to post notifications for children of this PIDL. For example, if the PIDL points to a folder, then file notifications would come from the folder's children if this flag was <b>TRUE</b>.