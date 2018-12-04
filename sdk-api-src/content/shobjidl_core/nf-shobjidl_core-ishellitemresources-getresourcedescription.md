---
UID: NF:shobjidl_core.IShellItemResources.GetResourceDescription
title: IShellItemResources::GetResourceDescription
author: windows-sdk-content
description: Gets a resource description.
old-location: shell\IShellItemResources_GetResourceDescription.htm
tech.root: shell
ms.assetid: f5e20d50-510d-4d30-903e-6953846957a9
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetResourceDescription, GetResourceDescription method [Windows Shell], GetResourceDescription method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],GetResourceDescription method, IShellItemResources.GetResourceDescription, IShellItemResources::GetResourceDescription, _shell_IShellItemResources_GetResourceDescription, shell.IShellItemResources_GetResourceDescription, shobjidl_core/IShellItemResources::GetResourceDescription
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
 - IShellItemResources.GetResourceDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemResources::GetResourceDescription


## -description


Gets a resource description.


## -parameters




### -param pcsir

Type: <b>const <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a> resource.


### -param ppszDescription [out]

Type: <b>LPWSTR*</b>

A pointer to a resource description as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



