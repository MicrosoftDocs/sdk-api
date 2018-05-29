---
UID: NF:shobjidl_core.ITransferSource.GetDefaultDestinationName
title: ITransferSource::GetDefaultDestinationName
author: windows-sdk-content
description: Gets the default name for a Shell item.
old-location: shell\ITransferSource_GetDefaultDestinationName.htm
old-project: shell
ms.assetid: a99d9622-b205-4a8a-9840-879f655463a5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDefaultDestinationName, GetDefaultDestinationName method [Windows Shell], GetDefaultDestinationName method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],GetDefaultDestinationName method, ITransferSource.GetDefaultDestinationName, ITransferSource::GetDefaultDestinationName, _shell_ITransferSource_GetDefaultDestinationName, shell.ITransferSource_GetDefaultDestinationName, shobjidl_core/ITransferSource::GetDefaultDestinationName
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ITransferSource.GetDefaultDestinationName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ITransferSource::GetDefaultDestinationName


## -description


Gets the default name for a Shell item.


## -parameters




### -param psiSource [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param psiParentDest [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the parent <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> of the destination target of the file operation.


### -param ppszDestinationName [out]

Type: <b>LPWSTR*</b>

When the method returns, contains a pointer to a null-terminated, Unicode string containing the default name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Gets the default name for a Shell item, if different than the item's parsing name.



