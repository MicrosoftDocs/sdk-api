---
UID: NF:wsman.WSManCloseOperation
title: WSManCloseOperation function (wsman.h)
description: Cancels or closes an asynchronous operation.
helpviewer_keywords: ["WSManCloseOperation","WSManCloseOperation function [Windows Remote Management]","winrm.wsmancloseoperation","wsman/WSManCloseOperation"]
old-location: winrm\wsmancloseoperation.htm
tech.root: winrm
ms.assetid: 4fd51026-6a48-42ef-a245-7593a615c103
ms.date: 12/05/2018
ms.keywords: WSManCloseOperation, WSManCloseOperation function [Windows Remote Management], winrm.wsmancloseoperation, wsman/WSManCloseOperation
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManCloseOperation
 - wsman/WSManCloseOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManCloseOperation
---

# WSManCloseOperation function


## -description

Cancels or closes an asynchronous operation. All resources that are associated with the operation are freed.

## -parameters

### -param operationHandle [in, out, optional]

Specifies the operation handle to be closed.

### -param flags

Reserved for future use. Set to zero.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.

## -remarks

The method de-allocates local and remote resources associated with the operation. After the <b>WSManCloseOperation</b> method is called, the <i>operationHandle</i> parameter cannot be passed to any other call. If the callback associated with the operation is pending and has not completed before <b>WSManCloseOperation</b> is called, the operation is marked for deletion and the method returns immediately.

