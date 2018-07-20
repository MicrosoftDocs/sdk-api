---
UID: NF:shobjidl_core.IShellItem2.GetCLSID
title: IShellItem2::GetCLSID
author: windows-sdk-content
description: Gets the class identifier (CLSID) value of specified property key.
old-location: shell\IShellItem2_GetCLSID.htm
old-project: shell
ms.assetid: 95b0c5fb-db09-4db0-8253-708f2dc2944b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetCLSID, GetCLSID method [Windows Shell], GetCLSID method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetCLSID method, IShellItem2.GetCLSID, IShellItem2::GetCLSID, _shell_IShellItem2_GetCLSID, shell.IShellItem2_GetCLSID, shobjidl_core/IShellItem2::GetCLSID
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
 - IShellItem2.GetCLSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem2::GetCLSID


## -description


Gets the class identifier (CLSID) value of specified property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param pclsid [out]

Type: <b>CLSID*</b>


          A pointer to a CLSID value.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



