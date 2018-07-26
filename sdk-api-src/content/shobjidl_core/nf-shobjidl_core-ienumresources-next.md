---
UID: NF:shobjidl_core.IEnumResources.Next
title: IEnumResources::Next
author: windows-sdk-content
description: Gets the next SHELL_ITEM_RESOURCE structure.
old-location: shell\IEnumResources_Next.htm
old-project: shell
ms.assetid: b5d0d754-4252-476a-b3af-0ba257eab339
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IEnumResources interface [Windows Shell],Next method, IEnumResources.Next, IEnumResources::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumResources interface, _shell_IEnumResources_Next, shell.IEnumResources_Next, shobjidl_core/IEnumResources::Next
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
 - IEnumResources.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IEnumResources::Next


## -description


Gets the next <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a> structure.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of resources requested. Currently, must be 1.


### -param psir [out]

Type: <b><a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a>*</b>

Receives a pointer to a <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a> structure.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of resources retrieved. Currently, not used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



