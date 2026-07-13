---
UID: NF:keycredmgr.KeyCredentialManagerGetOperationErrorStates
title: KeyCredentialManagerGetOperationErrorStates function (keycredmgr.h)
description: Prerequisite API to call to determine if the operation will be successful prior.
helpviewer_keywords: ["KeyCredentialManagerGetOperationErrorStates","KeyCredentialManagerGetOperationErrorStates function [Security]","keycredmgr/KeyCredentialManagerGetOperationErrorStates","security.keycredentialmanagergetoperationerrorstates"]
old-location: security\keycredentialmanagergetoperationerrorstates.htm
tech.root: security
ms.assetid: 0E34340F-D886-4E69-9AF3-D9142E350173
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerGetOperationErrorStates, KeyCredentialManagerGetOperationErrorStates function [Security], keycredmgr/KeyCredentialManagerGetOperationErrorStates, security.keycredentialmanagergetoperationerrorstates
req.header: keycredmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Keycredmgr.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KeyCredentialManagerGetOperationErrorStates
 - keycredmgr/KeyCredentialManagerGetOperationErrorStates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - keycredmgr.lib
 - keycredmgr.dll
api_name:
 - KeyCredentialManagerGetOperationErrorStates
---

# KeyCredentialManagerGetOperationErrorStates function


## -description

Prerequisite API to call to determine if the operation will be successful prior.

## -parameters

### -param keyCredentialManagerOperationType [in]

The intended operation from the <a href="../keycredmgr/ne-keycredmgr-keycredentialmanageroperationtype.md">KeyCredentialManagerOperationType</a>.

### -param isReady [out]

If the operational prerequisite will succeed (True) or (False).

### -param keyCredentialManagerOperationErrorStates [out]

Additional feedback about isReady represented by <a href="../keycredmgr/ne-keycredmgr-keycredentialmanageroperationerrorstates.md">KeyCredentialManagerOperationErrorStates</a>.

## -returns

Returns an HRESULT.

