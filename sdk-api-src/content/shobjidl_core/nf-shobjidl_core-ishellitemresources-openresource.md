---
UID: NF:shobjidl_core.IShellItemResources.OpenResource
title: IShellItemResources::OpenResource
author: windows-sdk-content
description: Opens a specified resource.
old-location: shell\IShellItemResources_OpenResource.htm
old-project: shell
ms.assetid: abef9009-7e0d-4a09-aba8-2b391e4ab487
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IShellItemResources interface [Windows Shell],OpenResource method, IShellItemResources.OpenResource, IShellItemResources::OpenResource, OpenResource, OpenResource method [Windows Shell], OpenResource method [Windows Shell],IShellItemResources interface, _shell_IShellItemResources_OpenResource, shell.IShellItemResources_OpenResource, shobjidl_core/IShellItemResources::OpenResource
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
 - IShellItemResources.OpenResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItemResources::OpenResource


## -description


Opens a specified resource.


## -parameters




### -param pcsir [in]

Type: <b>const <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a> resource.


### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired IID.


### -param ppv [out]

Type: <b>void**</b>

The address of a pointer to a resource.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



