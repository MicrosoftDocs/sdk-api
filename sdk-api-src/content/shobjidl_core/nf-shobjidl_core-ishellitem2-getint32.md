---
UID: NF:shobjidl_core.IShellItem2.GetInt32
title: IShellItem2::GetInt32
author: windows-sdk-content
description: Gets the Int32 value of specified property key.
old-location: shell\IShellItem2_GetInt32.htm
old-project: shell
ms.assetid: 7b56036e-316b-4300-979c-151422f74bd2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetInt32, GetInt32 method [Windows Shell], GetInt32 method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetInt32 method, IShellItem2.GetInt32, IShellItem2::GetInt32, _shell_IShellItem2_GetInt32, shell.IShellItem2_GetInt32, shobjidl_core/IShellItem2::GetInt32
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
 - IShellItem2.GetInt32
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem2::GetInt32


## -description


Gets the Int32 value of specified property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>


          A reference to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.
        


### -param pi [out]

Type: <b>int*</b>

A pointer to an Int32 value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



