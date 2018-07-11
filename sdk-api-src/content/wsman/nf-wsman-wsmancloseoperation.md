---
UID: NF:wsman.WSManCloseOperation
title: WSManCloseOperation function
author: windows-sdk-content
description: Cancels or closes an asynchronous operation.
old-location: winrm\wsmancloseoperation.htm
old-project: winrm
ms.assetid: 4fd51026-6a48-42ef-a245-7593a615c103
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: WSManCloseOperation, WSManCloseOperation function [Windows Remote Management], winrm.wsmancloseoperation, wsman/WSManCloseOperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSManSessionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManCloseOperation
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



