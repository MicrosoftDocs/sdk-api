---
UID: NF:shobjidl_core.IFolderView2.GetCurrentFolderFlags
title: IFolderView2::GetCurrentFolderFlags
author: windows-sdk-content
description: Gets the currently applied folder flags.
old-location: shell\IFolderView2_GetCurrentFolderFlags.htm
tech.root: shell
ms.assetid: 334d93c7-79a5-46c0-9042-400504aa2706
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetCurrentFolderFlags, GetCurrentFolderFlags method [Windows Shell], GetCurrentFolderFlags method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetCurrentFolderFlags method, IFolderView2.GetCurrentFolderFlags, IFolderView2::GetCurrentFolderFlags, _shell_IFolderView2_GetCurrentFolderFlags, shell.IFolderView2_GetCurrentFolderFlags, shobjidl_core/IFolderView2::GetCurrentFolderFlags
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
 - IFolderView2.GetCurrentFolderFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderView2::GetCurrentFolderFlags


## -description


Gets the currently applied folder flags.


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> with any <a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a> that have been applied to the folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



