---
UID: NF:shobjidl_core.IShellItemResources.SupportsResource
title: IShellItemResources::SupportsResource
author: windows-sdk-content
description: Retrieves whether an item supports a specified resource.
old-location: shell\IShellItemResources_SupportsResource.htm
old-project: shell
ms.assetid: d4ef7190-0056-423b-b958-bf746a66462d
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IShellItemResources interface [Windows Shell],SupportsResource method, IShellItemResources.SupportsResource, IShellItemResources::SupportsResource, SupportsResource, SupportsResource method [Windows Shell], SupportsResource method [Windows Shell],IShellItemResources interface, _shell_IShellItemResources_SupportsResource, shell.IShellItemResources_SupportsResource, shobjidl_core/IShellItemResources::SupportsResource
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
 - IShellItemResources.SupportsResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItemResources::SupportsResource


## -description


Retrieves whether an item supports a specified resource.


## -parameters




### -param pcsir [in]

Type: <b>const <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a> resource.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



