---
UID: NF:shobjidl_core.SHGetNameFromIDList
title: SHGetNameFromIDList function
author: windows-sdk-content
description: Retrieves the display name of an item identified by its IDList.
old-location: shell\SHGetNameFromIDList.htm
old-project: shell
ms.assetid: d2fc1eeb-bd76-4bd7-9a4f-4142e53f0afb
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: SHGetNameFromIDList, SHGetNameFromIDList function [Windows Shell], _shell_SHGetNameFromIDList, shell.SHGetNameFromIDList, shobjidl_core/SHGetNameFromIDList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHGetNameFromIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHGetNameFromIDList function


## -description


Retrieves the display name of an item identified by its IDList.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that identifies the item.


### -param sigdnName [in]

Type: <b><a href="https://msdn.microsoft.com/ef800ed8-8694-4543-ad33-c81b976cc5c2">SIGDN</a></b>

A value from the <a href="https://msdn.microsoft.com/ef800ed8-8694-4543-ad33-c81b976cc5c2">SIGDN</a> enumeration that specifies the type of display name to retrieve.


### -param ppszName [out]

Type: <b>PWSTR*</b>

A value that, when this function returns successfully, receives the address of a pointer to the retrieved display name.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is the responsibility of the caller to free the string pointed to by <i>ppszName</i> when it is no longer needed. Call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> on *<i>ppszName</i> to free the memory.



