---
UID: NF:shlobj.ICurrentWorkingDirectory.GetDirectory
title: ICurrentWorkingDirectory::GetDirectory
author: windows-sdk-content
description: Gets the current working directory.
old-location: shell\ICurrentWorkingDirectory_GetDirectory.htm
tech.root: Shell
ms.assetid: 763c042b-2780-4202-9c3e-073cc8adc93a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetDirectory, GetDirectory method [Windows Shell], GetDirectory method [Windows Shell],ICurrentWorkingDirectory interface, ICurrentWorkingDirectory interface [Windows Shell],GetDirectory method, ICurrentWorkingDirectory.GetDirectory, ICurrentWorkingDirectory::GetDirectory, _win32_ICurrentWorkingDirectory_GetDirectory, shell.ICurrentWorkingDirectory_GetDirectory, shlobj/ICurrentWorkingDirectory::GetDirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICurrentWorkingDirectory.GetDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICurrentWorkingDirectory::GetDirectory


## -description


Gets the current working directory.


## -parameters




### -param pwzPath [out]

Type: <b>PWSTR</b>

Pointer to a buffer that, when this method returns successfully, receives the current working directory's fully qualified path as a null-terminated Unicode string.


### -param cchSize

Type: <b>DWORD</b>

The size of the buffer in Unicode characters, including the terminating <b>NULL</b> character.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



