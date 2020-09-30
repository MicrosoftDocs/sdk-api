---
UID: NF:wsman.WSManInitialize
title: WSManInitialize function (wsman.h)
description: Initializes the Windows Remote Management Client API.
helpviewer_keywords: ["WSManInitialize","WSManInitialize function [Windows Remote Management]","winrm.wsmaninitialize","wsman/WSManInitialize"]
old-location: winrm\wsmaninitialize.htm
tech.root: winrm
ms.assetid: 5aa1f451-0d12-4079-9477-1971fc084df2
ms.date: 12/05/2018
ms.keywords: WSManInitialize, WSManInitialize function [Windows Remote Management], winrm.wsmaninitialize, wsman/WSManInitialize
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - WSManInitialize
 - wsman/WSManInitialize
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
 - WSManInitialize
---

# WSManInitialize function


## -description

Initializes the Windows Remote Management Client API. <b>WSManInitialize</b> can be used by different clients on the same process.

## -parameters

### -param flags

A flag of type <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_0</b> or <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b>.
The client that will use the disconnect-reconnect functionality should use the 
<b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b> flag.

### -param apiHandle [out]

Defines a handle that uniquely identifies the client. This parameter cannot be <b>NULL</b>. When you have finished used the handle, close it by calling the <a href="/windows/desktop/api/wsman/nf-wsman-wsmandeinitialize">WSManDeinitialize</a> method.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.