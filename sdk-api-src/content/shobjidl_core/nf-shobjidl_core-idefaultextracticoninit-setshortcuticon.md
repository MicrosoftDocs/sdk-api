---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetShortcutIcon
title: IDefaultExtractIconInit::SetShortcutIcon
author: windows-sdk-content
description: Sets the icon for a shortcut to the object.
old-location: shell\IDefaultExtractIconInit_SetShortcutIcon.htm
tech.root: shell
ms.assetid: 1defab08-3dce-4668-aca3-d11821a4c339
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetShortcutIcon method, IDefaultExtractIconInit.SetShortcutIcon, IDefaultExtractIconInit::SetShortcutIcon, SetShortcutIcon, SetShortcutIcon method [Windows Shell], SetShortcutIcon method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetShortcutIcon, shell.IDefaultExtractIconInit_SetShortcutIcon, shobjidl_core/IDefaultExtractIconInit::SetShortcutIcon
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
 - IDefaultExtractIconInit.SetShortcutIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDefaultExtractIconInit::SetShortcutIcon


## -description


Sets the icon for a shortcut to the object.


## -parameters




### -param pszFile [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the full icon path, including the file name and extension, as a Unicode string. This pointer can be <b>NULL</b>.


### -param iIcon

Type: <b>int</b>

Shell icon ID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



