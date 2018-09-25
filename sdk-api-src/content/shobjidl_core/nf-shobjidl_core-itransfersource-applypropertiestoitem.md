---
UID: NF:shobjidl_core.ITransferSource.ApplyPropertiesToItem
title: ITransferSource::ApplyPropertiesToItem
author: windows-sdk-content
description: Apply a set of property changes to an item.
old-location: shell\ITransferSource_ApplyPropertiesToItem.htm
tech.root: shell
ms.assetid: f3a99637-8ce7-4177-bcf7-716ed7698934
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ApplyPropertiesToItem, ApplyPropertiesToItem method [Windows Shell], ApplyPropertiesToItem method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],ApplyPropertiesToItem method, ITransferSource.ApplyPropertiesToItem, ITransferSource::ApplyPropertiesToItem, _shell_ITransferSource_ApplyPropertiesToItem, shell.ITransferSource_ApplyPropertiesToItem, shobjidl_core/ITransferSource::ApplyPropertiesToItem
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
 - ITransferSource.ApplyPropertiesToItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferSource::ApplyPropertiesToItem


## -description


Apply a set of property changes to an item.


## -parameters




### -param psiSource [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> to be altered.


### -param ppsiNew [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When this method returns, contains the address of a pointer to the changed <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



