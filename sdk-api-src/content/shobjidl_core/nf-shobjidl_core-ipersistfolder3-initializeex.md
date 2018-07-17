---
UID: NF:shobjidl_core.IPersistFolder3.InitializeEx
title: IPersistFolder3::InitializeEx
author: windows-sdk-content
description: Initializes a folder and specifies its location in the namespace. If the folder is a shortcut, this method also specifies the location of the target folder.
old-location: shell\IPersistFolder3_InitializeEx.htm
old-project: shell
ms.assetid: 50a426b5-a526-4d3d-a20a-67050229f02e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IPersistFolder3 interface [Windows Shell],InitializeEx method, IPersistFolder3.InitializeEx, IPersistFolder3::InitializeEx, InitializeEx, InitializeEx method [Windows Shell], InitializeEx method [Windows Shell],IPersistFolder3 interface, _win32_IPersistFolder3_InitializeEx, shell.IPersistFolder3_InitializeEx, shobjidl_core/IPersistFolder3::InitializeEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IPersistFolder3.InitializeEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IPersistFolder3::InitializeEx


## -description


Initializes a folder and specifies its location in the namespace. If the folder is a shortcut, this method also specifies the location of the target folder.


## -parameters




### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> object that provides the bind context. This parameter can be <b>NULL</b>.


### -param pidlRoot [in]

Type: <b>LPCITEMIDLIST</b>

A pointer to a fully qualified PIDL that specifies the absolute location of a folder or folder shortcut. The calling application is responsible for allocating and freeing this PIDL.


### -param ppfti [in]

Type: <b>const <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a> structure that specifies the location of the target folder and its attributes. 

                    

If <i>ppfti</i> points to a valid structure, <i>pidlRoot</i> represents a folder shortcut.

If <i>ppfti</i> is set to <b>NULL</b>, <i>pidlRoot</i> represents a normal folder. In that case, <b>InitializeEx</b> should behave as if <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> had been called.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is an extended version of <a href="https://msdn.microsoft.com/179f13c9-7306-4ed5-935e-2620616b46c1">IPersistFolder::Initialize</a>. It allows the Shell to initialize folder shortcuts as well as normal folders.



