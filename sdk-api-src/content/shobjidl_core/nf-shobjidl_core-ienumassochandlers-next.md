---
UID: NF:shobjidl_core.IEnumAssocHandlers.Next
title: IEnumAssocHandlers::Next
author: windows-sdk-content
description: Retrieves a specified number of elements.
old-location: shell\IEnumAssocHandlers_Next.htm
tech.root: shell
ms.assetid: 9e173cb3-bd73-437c-8853-c13c8b6f216f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IEnumAssocHandlers interface [Windows Shell],Next method, IEnumAssocHandlers.Next, IEnumAssocHandlers::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumAssocHandlers interface, _shell_IEnumAssocHandlers_Next, shell.IEnumAssocHandlers_Next, shobjidl_core/IEnumAssocHandlers::Next
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
 - IEnumAssocHandlers.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumAssocHandlers::Next


## -description


Retrieves a specified number of elements.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements to retrieve.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>**</b>

When this method returns, contains the address of an array of <a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a> pointers. Each <b>IAssocHandler</b> represents a single handler.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of elements retrieved.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



