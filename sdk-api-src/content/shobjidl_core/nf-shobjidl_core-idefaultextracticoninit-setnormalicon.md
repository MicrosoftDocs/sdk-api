---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetNormalIcon
title: IDefaultExtractIconInit::SetNormalIcon
author: windows-sdk-content
description: Sets the normal icon.
old-location: shell\IDefaultExtractIconInit_SetNormalIcon.htm
old-project: shell
ms.assetid: 49d11767-4237-48f3-973b-03cf032c5e68
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetNormalIcon method, IDefaultExtractIconInit.SetNormalIcon, IDefaultExtractIconInit::SetNormalIcon, SetNormalIcon, SetNormalIcon method [Windows Shell], SetNormalIcon method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetNormalIcon, shell.IDefaultExtractIconInit_SetNormalIcon, shobjidl_core/IDefaultExtractIconInit::SetNormalIcon
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDefaultExtractIconInit.SetNormalIcon
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDefaultExtractIconInit::SetNormalIcon


## -description


Sets the normal icon.


## -parameters




### -param pszFile [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the full icon path, including the file name and extension, as a Unicode string. This pointer can be <b>NULL</b>.


### -param iIcon

Type: <b>int</b>

A Shell icon ID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



