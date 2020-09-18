---
UID: NF:wsman.WSManDeinitialize
title: WSManDeinitialize function (wsman.h)
description: Deinitializes the Windows Remote Management client stack.
helpviewer_keywords: ["WSManDeinitialize","WSManDeinitialize function [Windows Remote Management]","winrm.wsmandeinitialize","wsman/WSManDeinitialize"]
old-location: winrm\wsmandeinitialize.htm
tech.root: winrm
ms.assetid: 1b20ead1-cda0-4449-a454-1e695fe71de6
ms.date: 12/05/2018
ms.keywords: WSManDeinitialize, WSManDeinitialize function [Windows Remote Management], winrm.wsmandeinitialize, wsman/WSManDeinitialize
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
 - WSManDeinitialize
 - wsman/WSManDeinitialize
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
 - WSManDeinitialize
---

# WSManDeinitialize function


## -description

Deinitializes the Windows Remote Management client stack. All operations must be complete before a call to this function will return. This is a synchronous call. It is recommended that all operations are explicitly canceled and that all sessions are closed before calling this function.

## -parameters

### -param apiHandle [in, out, optional]

Specifies the API handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmaninitialize">WSManInitialize</a> call. This parameter cannot be <b>NULL</b>.

### -param flags

Reserved for future use. Must be zero.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.