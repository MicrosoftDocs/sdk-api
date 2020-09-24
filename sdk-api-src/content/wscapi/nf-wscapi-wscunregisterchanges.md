---
UID: NF:wscapi.WscUnRegisterChanges
title: WscUnRegisterChanges function (wscapi.h)
description: Cancels a callback registration that was made by a call to the WscRegisterForChanges function.
helpviewer_keywords: ["WscUnRegisterChanges","WscUnRegisterChanges function [Windows API]","winprog.wscunregisterchanges","wscapi/WscUnRegisterChanges"]
old-location: winprog\wscunregisterchanges.htm
tech.root: winprog
ms.assetid: cfb0d076-bd8b-4483-a036-51c77b8181c9
ms.date: 12/05/2018
ms.keywords: WscUnRegisterChanges, WscUnRegisterChanges function [Windows API], winprog.wscunregisterchanges, wscapi/WscUnRegisterChanges
req.header: wscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WscUnRegisterChanges
 - wscapi/WscUnRegisterChanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wscapi.dll
api_name:
 - WscUnRegisterChanges
---

# WscUnRegisterChanges function


## -description

Cancels a callback registration that was made by a call to the <a href="/windows/desktop/api/wscapi/nf-wscapi-wscregisterforchanges">WscRegisterForChanges</a> function.

## -parameters

### -param hRegistrationHandle [in]

The handle to the registration context returned as the <i>phCallbackRegistration</i> of the <a href="/windows/desktop/api/wscapi/nf-wscapi-wscregisterforchanges">WscRegisterForChanges</a> function.

## -returns

Returns <b>S_OK</b> if the function succeeds, otherwise returns an error code.

## -see-also

<a href="/windows/desktop/api/wscapi/nf-wscapi-wscregisterforchanges">WscRegisterForChanges</a>