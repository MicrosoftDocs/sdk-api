---
UID: NF:shobjidl_core.SHGetTemporaryPropertyForItem
title: SHGetTemporaryPropertyForItem function
author: windows-sdk-content
description: Retrieves the temporary property for the given item. A temporary property is a read/write store that holds properties only for the lifetime of the IShellItem object, rather than being persisted back into the item.
old-location: shell\SHGetTemporaryPropertyForItem.htm
old-project: shell
ms.assetid: 53953a5a-04a2-4749-a03b-8cbd5ac889f1
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SHGetTemporaryPropertyForItem, SHGetTemporaryPropertyForItem function [Windows Shell], _shell_SHGetTemporaryPropertyForItem, shell.SHGetTemporaryPropertyForItem, shobjidl_core/SHGetTemporaryPropertyForItem
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
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHGetTemporaryPropertyForItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHGetTemporaryPropertyForItem function


## -description


Retrieves the temporary property for the given item. A temporary property is a read/write store that holds properties only for the lifetime of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object, rather than being persisted back into the item.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the item for which the temporary property is to be retrieved.


### -param propkey

TBD


### -param ppropvar

TBD




#### - pk

Type: <b>REFPROPERTYKEY</b>

The property key.


#### - ppropvarInk [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A pointer to the temporary property for the item.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



