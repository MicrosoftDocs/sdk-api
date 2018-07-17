---
UID: NF:shobjidl_core.SHCreateItemWithParent
title: SHCreateItemWithParent function
author: windows-sdk-content
description: Create a Shell item, given a parent folder and a child item ID.
old-location: shell\SHCreateItemWithParent.htm
old-project: shell
ms.assetid: 8fb84a20-d8f2-4c7c-bfb1-a22791b8636a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: SHCreateItemWithParent, SHCreateItemWithParent function [Windows Shell], _shell_SHCreateItemWithParent, shell.SHCreateItemWithParent, shobjidl_core/SHCreateItemWithParent
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
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHCreateItemWithParent
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHCreateItemWithParent function


## -description


Create a Shell item, given a parent folder and a child item ID.


## -parameters




### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The IDList of the parent folder of the item being created; the IDList of <i>psfParent</i>. This parameter can be <b>NULL</b>, if <i>psfParent</i> is specified.


### -param psfParent [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface that specifies the shell data source of the child item specified by the <i>pidl</i>.This parameter can be <b>NULL</b>, if <i>pidlParent</i> is specified.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A child item ID relative to its parent folder specified by <i>psfParent</i> or <i>pidlParent</i>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to an interface ID.


### -param ppvItem [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid.  This will typically be <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or 
        <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



