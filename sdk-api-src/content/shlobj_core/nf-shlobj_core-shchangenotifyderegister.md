---
UID: NF:shlobj_core.SHChangeNotifyDeregister
title: SHChangeNotifyDeregister function
author: windows-sdk-content
description: Unregisters the client's window process from receiving SHChangeNotify messages.
old-location: shell\SHChangeNotifyDeregister.htm
old-project: shell
ms.assetid: fad021dc-8199-4384-b623-c98bc618799f
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: NTSHChangeNotifyDeregister, SHChangeNotifyDeregister, SHChangeNotifyDeregister function [Windows Shell], _win32_SHChangeNotifyDeregister, shell.SHChangeNotifyDeregister, shlobj_core/NTSHChangeNotifyDeregister, shlobj_core/SHChangeNotifyDeregister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - SHChangeNotifyDeregister
 - NTSHChangeNotifyDeregister
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHChangeNotifyDeregister function


## -description


Unregisters the client's window process from receiving <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> messages.


## -parameters




### -param ulID

Type: <b>ULONG</b>

A value of type <b>ULONG</b> that specifies the registration ID returned by <a href="https://msdn.microsoft.com/73143865-ca2f-4578-a7a2-2ba4833eddd8">SHChangeNotifyRegister</a>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the specified client was found and removed; otherwise <b>FALSE</b>.




## -remarks



See the <a href="https://msdn.microsoft.com/02A7C5B4-94F2-4c35-9290-4C816E5CF63A">Change Notify Watcher Sample</a> in the Windows Software Development Kit (SDK) for a full example that demonstrates the use of this function.

The <b>NTSHChangeNotifyDeregister</b> function, which is no longer available for use as of Windows Vista, was equivalent to <b>SHChangeNotifyDeregister</b>.



