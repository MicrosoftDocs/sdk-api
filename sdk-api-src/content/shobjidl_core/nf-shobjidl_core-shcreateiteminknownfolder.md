---
UID: NF:shobjidl_core.SHCreateItemInKnownFolder
title: SHCreateItemInKnownFolder function
author: windows-sdk-content
description: Creates a Shell item object for a single file that exists inside a known folder.
old-location: shell\SHCreateItemInKnownFolder.htm
tech.root: shell
ms.assetid: dc75ee60-7319-4a11-949e-dd0c3deabd8f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SHCreateItemInKnownFolder, SHCreateItemInKnownFolder function [Windows Shell], _shell_SHCreateItemInKnownFolder, shell.SHCreateItemInKnownFolder, shobjidl_core/SHCreateItemInKnownFolder
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
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - SHCreateItemInKnownFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateItemInKnownFolder function


## -description


Creates a Shell item object for a single file that exists inside a known folder.


## -parameters




### -param kfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>, a <b>GUID</b> that identifies the folder that contains the item.


### -param dwKFFlags

Type: <b>DWORD</b>

Flags that specify special options in the object retrieval. This value can be 0; otherwise, one or more of the <a href="https://msdn.microsoft.com/7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1">KNOWN_FOLDER_FLAG</a> values.


### -param pszItem [in, optional]

Type: <b>PCWSTR</b>

A pointer to a null-terminated buffer that contains the file name of the new item as a Unicode string. This parameter can also be <b>NULL</b>. In this case, an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the known folder itself is created.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface that represents the item, retrieved through <i>ppv</i>. This value is typically IID_IShellItem or IID_IShellItem2.


### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

