---
UID: NF:shlobj.ICurrentWorkingDirectory.SetDirectory
title: ICurrentWorkingDirectory::SetDirectory (shlobj.h)
description: Sets the current working directory.
old-location: shell\ICurrentWorkingDirectory_SetDirectory.htm
tech.root: shell
ms.assetid: cd7d1517-8c0c-4e42-b750-815fa0aff32c
ms.date: 12/05/2018
ms.keywords: ICurrentWorkingDirectory interface [Windows Shell],SetDirectory method, ICurrentWorkingDirectory.SetDirectory, ICurrentWorkingDirectory::SetDirectory, SetDirectory, SetDirectory method [Windows Shell], SetDirectory method [Windows Shell],ICurrentWorkingDirectory interface, _win32_ICurrentWorkingDirectory_SetDirectory, shell.ICurrentWorkingDirectory_SetDirectory, shlobj/ICurrentWorkingDirectory::SetDirectory
f1_keywords:
- shlobj/ICurrentWorkingDirectory.SetDirectory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- ICurrentWorkingDirectory.SetDirectory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory">ICurrentWorkingDirectory</a>
 

 

