---
UID: NF:shobjidl_core.ITransferAdviseSink.UpdateTransferState
title: ITransferAdviseSink::UpdateTransferState
author: windows-sdk-content
description: Updates the transfer state.
old-location: shell\ITransferAdviseSink_UpdateTransferState.htm
old-project: shell
ms.assetid: 37e830b0-a426-4a66-83c3-108f315f50ac
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITransferAdviseSink interface [Windows Shell],UpdateTransferState method, ITransferAdviseSink.UpdateTransferState, ITransferAdviseSink::UpdateTransferState, TS_INDETERMINATE, TS_NONE, TS_PERFORMING, TS_PREPARING, UpdateTransferState, UpdateTransferState method [Windows Shell], UpdateTransferState method [Windows Shell],ITransferAdviseSink interface, _shell_ITransferAdviseSink_UpdateTransferState, shell.ITransferAdviseSink_UpdateTransferState, shobjidl_core/ITransferAdviseSink::UpdateTransferState
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ITransferAdviseSink.UpdateTransferState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ITransferAdviseSink::UpdateTransferState


## -description


Updates the transfer state.


## -parameters




### -param ts [in]

Type: <b>TRANSFER_ADVISE_STATE</b>

The transfer state. One of the following values.



#### TS_NONE (0x00000000)

0x00000000. No transfer is in progress.



#### TS_PERFORMING (0x00000001)

0x00000001. The transfer is being performed.



#### TS_PREPARING (0x00000002)

0x00000002. The transfer is preparing to begin. For example, this flag would be set when space requirements are being calculated.



#### TS_INDETERMINATE (0x00000004)

0x00000004. Length of the transfer is unknown.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



