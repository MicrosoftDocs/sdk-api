---
UID: NF:shldisp.IShellFolderViewDual3.get_FolderFlags
title: IShellFolderViewDual3::get_FolderFlags
author: windows-driver-content
description: Gets the settings for the current folder.
old-location: shell\IShellFolderViewDual3_get_FolderFlags.htm
old-project: shell
ms.assetid: c0fc82d4-d27e-4410-88a8-83839de8409b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],get_FolderFlags method, IShellFolderViewDual3.get_FolderFlags, IShellFolderViewDual3::get_FolderFlags, _shell_IShellFolderViewDual3_get_FolderFlags, get_FolderFlags, get_FolderFlags method [Windows Shell], get_FolderFlags method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_get_FolderFlags, shldisp/IShellFolderViewDual3::get_FolderFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shldisp.h
api_name:
-	IShellFolderViewDual3.get_FolderFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderViewDual3::get_FolderFlags


## -description


Gets the settings for the current folder.


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to the current setting flags.  For a list of possible values, see <a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



