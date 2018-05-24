---
UID: NF:shobjidl_core.IShellItem2.GetBool
title: IShellItem2::GetBool
author: windows-driver-content
description: Gets the boolean value of a specified property key.
old-location: shell\IShellItem2_GetBool.htm
old-project: shell
ms.assetid: 754d0a7a-a6b4-41ef-8c8f-483539f7d53e
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetBool, GetBool method [Windows Shell], GetBool method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetBool method, IShellItem2.GetBool, IShellItem2::GetBool, _shell_IShellItem2_GetBool, shell.IShellItem2_GetBool, shobjidl_core/IShellItem2::GetBool
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IShellItem2.GetBool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem2::GetBool


## -description


Gets the boolean value of a specified property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param pf [out]

Type: <b>BOOL*</b>

A pointer to a boolean value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



