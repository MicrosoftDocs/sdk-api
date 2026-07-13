---
UID: NF:shobjidl_core.IEnumExplorerCommand.Next
title: IEnumExplorerCommand::Next (shobjidl_core.h)
description: Retrieves a specified number of elements that directly follow the current element.
helpviewer_keywords: ["IEnumExplorerCommand interface [Windows Shell]","Next method","IEnumExplorerCommand.Next","IEnumExplorerCommand::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumExplorerCommand interface","_shell_IEnumExplorerCommand_Next","shell.IEnumExplorerCommand_Next","shobjidl_core/IEnumExplorerCommand::Next"]
old-location: shell\IEnumExplorerCommand_Next.htm
tech.root: shell
ms.assetid: 809e866d-128b-4a0e-9de0-c2123161134f
ms.date: 12/05/2018
ms.keywords: IEnumExplorerCommand interface [Windows Shell],Next method, IEnumExplorerCommand.Next, IEnumExplorerCommand::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumExplorerCommand interface, _shell_IEnumExplorerCommand_Next, shell.IEnumExplorerCommand_Next, shobjidl_core/IEnumExplorerCommand::Next
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumExplorerCommand::Next
 - shobjidl_core/IEnumExplorerCommand::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumExplorerCommand.Next
---

# IEnumExplorerCommand::Next


## -description

Retrieves a specified number of elements that directly follow the current element.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of elements to fetch.

### -param pUICommand [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand">IExplorerCommand</a>**</b>

Address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand">IExplorerCommand</a> interface pointer array of <i>celt</i> elements that, when this method returns, is an array of pointers to the retrieved elements.

### -param pceltFetched [out, optional]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of elements actually retrieved. This pointer can be <b>NULL</b> if this information is not needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.