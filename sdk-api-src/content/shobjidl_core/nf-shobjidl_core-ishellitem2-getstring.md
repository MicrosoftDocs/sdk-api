---
UID: NF:shobjidl_core.IShellItem2.GetString
title: IShellItem2::GetString
author: windows-sdk-content
description: Gets the string value of a specified property key.
old-location: shell\IShellItem2_GetString.htm
old-project: shell
ms.assetid: 912b3653-340b-4186-b652-53d958534c1d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetString, GetString method [Windows Shell], GetString method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetString method, IShellItem2.GetString, IShellItem2::GetString, _shell_IShellItem2_GetString, shell.IShellItem2_GetString, shobjidl_core/IShellItem2::GetString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IShellItem2.GetString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem2::GetString


## -description


Gets the string value of a specified property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param ppsz [out]

Type: <b>LPWSTR*</b>

A pointer to a Unicode string value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



