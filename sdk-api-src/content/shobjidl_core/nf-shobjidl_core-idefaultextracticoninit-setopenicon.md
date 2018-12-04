---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetOpenIcon
title: IDefaultExtractIconInit::SetOpenIcon
author: windows-sdk-content
description: Sets the icon that allows containers to specify an &#0034;open&#0034; look.
old-location: shell\IDefaultExtractIconInit_SetOpenIcon.htm
tech.root: shell
ms.assetid: 837a0006-2153-405f-a035-06738b89b058
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetOpenIcon method, IDefaultExtractIconInit.SetOpenIcon, IDefaultExtractIconInit::SetOpenIcon, SetOpenIcon, SetOpenIcon method [Windows Shell], SetOpenIcon method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetOpenIcon, shell.IDefaultExtractIconInit_SetOpenIcon, shobjidl_core/IDefaultExtractIconInit::SetOpenIcon
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
 - IDefaultExtractIconInit.SetOpenIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDefaultExtractIconInit::SetOpenIcon


## -description


Sets the icon that allows containers to specify an "open" look.


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



