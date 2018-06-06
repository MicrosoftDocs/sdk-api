---
UID: NF:shobjidl_core.IShellItem.GetDisplayName
title: IShellItem::GetDisplayName
author: windows-sdk-content
description: Gets the display name of the IShellItem object.
old-location: shell\IShellItem_GetDisplayName.htm
old-project: shell
ms.assetid: 9b159be9-3797-4c8b-90f8-9d3b3a3afb71
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDisplayName, GetDisplayName method [Windows Shell], GetDisplayName method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],GetDisplayName method, IShellItem.GetDisplayName, IShellItem::GetDisplayName, _win32_IShellItem_GetDisplayName, shell.IShellItem_GetDisplayName, shobjidl_core/IShellItem::GetDisplayName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shlguid.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellItem.GetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem::GetDisplayName


## -description


Gets the display name of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object.


## -parameters




### -param sigdnName [in]

Type: <b><a href="https://msdn.microsoft.com/ef800ed8-8694-4543-ad33-c81b976cc5c2">SIGDN</a></b>

One of the <a href="https://msdn.microsoft.com/ef800ed8-8694-4543-ad33-c81b976cc5c2">SIGDN</a> values that indicates how the name should look.


### -param ppszName [out]

Type: <b>LPWSTR*</b>

A value that, when this function returns successfully, receives the address of a pointer to the retrieved display name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is the responsibility of the caller to free the string pointed to by <i>ppszName</i> when it is no longer needed. Call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> on *<i>ppszName</i> to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

