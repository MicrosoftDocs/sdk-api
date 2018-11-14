---
UID: NF:shobjidl_core.SHCreateItemFromIDList
title: SHCreateItemFromIDList function
author: windows-sdk-content
description: Creates and initializes a Shell item object from a pointer to an item identifier list (PIDL). The resulting shell item object supports the IShellItem interface.
old-location: shell\SHCreateItemFromIDList.htm
tech.root: shell
ms.assetid: a6dcddd9-cdbc-4cf9-97e3-d1b562283344
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SHCreateItemFromIDList, SHCreateItemFromIDList function [Windows Shell], _shell_SHCreateItemFromIDList, shell.SHCreateItemFromIDList, shobjidl_core/SHCreateItemFromIDList
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
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
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHCreateItemFromIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SHCreateItemFromIDList
: 
---

# SHCreateItemFromIDList function


## -description


Creates and initializes a Shell item object from a pointer to an item identifier list (PIDL). The resulting shell item object supports the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interface.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The source PIDL.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid.  This will typically be <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or 
        <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/42821075-8123-4bfa-a6ba-8d3a77a9f50b">SHGetIDListFromObject</a>
 

 

