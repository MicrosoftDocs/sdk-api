---
UID: NS:shlobj_core._SHChangeNotifyEntry
title: "_SHChangeNotifyEntry"
author: windows-sdk-content
description: Contains and receives information for change notifications. This structure is used with the SHChangeNotifyRegister function and the SFVM_QUERYFSNOTIFY notification.
old-location: shell\SHChangeNotifyEntry.htm
tech.root: Shell
ms.assetid: cb11435a-86f0-4b06-bfc6-e0417f2897a1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: SHChangeNotifyEntry, SHChangeNotifyEntry structure [Windows Shell], _SHChangeNotifyEntry, _win32_SHChangeNotifyEntry, shell.SHChangeNotifyEntry, shlobj_core/SHChangeNotifyEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHChangeNotifyEntry
product: Windows
targetos: Windows
req.typenames: SHChangeNotifyEntry
req.redist: 
---

# _SHChangeNotifyEntry structure


## -description


Contains and receives information for change notifications. This structure is used with the <a href="https://msdn.microsoft.com/73143865-ca2f-4578-a7a2-2ba4833eddd8">SHChangeNotifyRegister</a> function and the <a href="https://msdn.microsoft.com/5d777115-bae3-47c4-9edc-c99c40a4f926">SFVM_QUERYFSNOTIFY</a> notification.


## -struct-fields




### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

PIDL for which to receive notifications.


### -field fRecursive

Type: <b>BOOL</b>

A flag indicating whether to post notifications for children of this PIDL. For example, if the PIDL points to a folder, then file notifications would come from the folder's children if this flag was <b>TRUE</b>.

