---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



