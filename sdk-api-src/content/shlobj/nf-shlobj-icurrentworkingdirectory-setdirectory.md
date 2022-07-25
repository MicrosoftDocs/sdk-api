---
UID: NF:shlobj.ICurrentWorkingDirectory.SetDirectory
title: ICurrentWorkingDirectory::SetDirectory (shlobj.h)
description: Sets the current working directory.
helpviewer_keywords: ["ICurrentWorkingDirectory interface [Windows Shell]","SetDirectory method","ICurrentWorkingDirectory.SetDirectory","ICurrentWorkingDirectory::SetDirectory","SetDirectory","SetDirectory method [Windows Shell]","SetDirectory method [Windows Shell]","ICurrentWorkingDirectory interface","_win32_ICurrentWorkingDirectory_SetDirectory","shell.ICurrentWorkingDirectory_SetDirectory","shlobj/ICurrentWorkingDirectory::SetDirectory"]
old-location: shell\ICurrentWorkingDirectory_SetDirectory.htm
tech.root: shell
ms.assetid: cd7d1517-8c0c-4e42-b750-815fa0aff32c
ms.date: 12/05/2018
ms.keywords: ICurrentWorkingDirectory interface [Windows Shell],SetDirectory method, ICurrentWorkingDirectory.SetDirectory, ICurrentWorkingDirectory::SetDirectory, SetDirectory, SetDirectory method [Windows Shell], SetDirectory method [Windows Shell],ICurrentWorkingDirectory interface, _win32_ICurrentWorkingDirectory_SetDirectory, shell.ICurrentWorkingDirectory_SetDirectory, shlobj/ICurrentWorkingDirectory::SetDirectory
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICurrentWorkingDirectory::SetDirectory
 - shlobj/ICurrentWorkingDirectory::SetDirectory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICurrentWorkingDirectory.SetDirectory
---

# ICurrentWorkingDirectory::SetDirectory


## -description

Sets the current working directory.

## -parameters

### -param pwzPath [in]

Type: <b>PCWSTR</b>

A pointer to the fully qualified path of the new working directory, as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory">ICurrentWorkingDirectory</a>