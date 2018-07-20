---
UID: NF:shobjidl_core.IEnumExplorerCommand.Next
title: IEnumExplorerCommand::Next
author: windows-sdk-content
description: Retrieves a specified number of elements that directly follow the current element.
old-location: shell\IEnumExplorerCommand_Next.htm
old-project: shell
ms.assetid: 809e866d-128b-4a0e-9de0-c2123161134f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IEnumExplorerCommand interface [Windows Shell],Next method, IEnumExplorerCommand.Next, IEnumExplorerCommand::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumExplorerCommand interface, _shell_IEnumExplorerCommand_Next, shell.IEnumExplorerCommand_Next, shobjidl_core/IEnumExplorerCommand::Next
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
 - IEnumExplorerCommand.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IEnumExplorerCommand::Next


## -description


Retrieves a specified number of elements that directly follow the current element.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of elements to fetch.


### -param pUICommand [out]

Type: <b><a href="https://msdn.microsoft.com/61e94e50-9e12-4a2c-a6c7-64a9181f80b8">IExplorerCommand</a>**</b>

Address of an <a href="https://msdn.microsoft.com/61e94e50-9e12-4a2c-a6c7-64a9181f80b8">IExplorerCommand</a> interface pointer array of <i>celt</i> elements that, when this method returns, is an array of pointers to the retrieved elements.


### -param pceltFetched [out, optional]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of elements actually retrieved. This pointer can be <b>NULL</b> if this information is not needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



