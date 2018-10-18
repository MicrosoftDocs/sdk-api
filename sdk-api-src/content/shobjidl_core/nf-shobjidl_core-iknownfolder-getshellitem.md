---
UID: NF:shobjidl_core.IKnownFolder.GetShellItem
title: IKnownFolder::GetShellItem
author: windows-sdk-content
description: Retrieves the location of a known folder in the Shell namespace in the form of a Shell item (IShellItem or derived interface).
old-location: shell\IKnownFolder_GetShellItem.htm
tech.root: shell
ms.assetid: a42c0a20-9c72-48d3-8432-15b73ff211d2
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetShellItem, GetShellItem method [Windows Shell], GetShellItem method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetShellItem method, IKnownFolder.GetShellItem, IKnownFolder::GetShellItem, _shell_IKnownFolder_GetShellItem, shell.IKnownFolder_GetShellItem, shobjidl_core/IKnownFolder::GetShellItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IKnownFolder.GetShellItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder::GetShellItem


## -description


Retrieves the location of a known folder in the Shell namespace in the form of a Shell item (<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or derived interface).


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="https://msdn.microsoft.com/7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1">KNOWN_FOLDER_FLAG</a> values.


### -param riid

Type: <b>REFIID</b>

A reference to the IID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

