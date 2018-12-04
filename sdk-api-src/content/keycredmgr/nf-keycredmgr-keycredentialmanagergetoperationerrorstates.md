---
UID: NF:keycredmgr.KeyCredentialManagerGetOperationErrorStates
title: KeyCredentialManagerGetOperationErrorStates function
author: windows-sdk-content
description: Prerequisite API to call to determine if the operation will be successful prior.
old-location: security\keycredentialmanagergetoperationerrorstates.htm
tech.root: secauthn
ms.assetid: 0E34340F-D886-4E69-9AF3-D9142E350173
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: KeyCredentialManagerGetOperationErrorStates, KeyCredentialManagerGetOperationErrorStates function [Security], keycredmgr/KeyCredentialManagerGetOperationErrorStates, security.keycredentialmanagergetoperationerrorstates
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# KeyCredentialManagerGetOperationErrorStates function


## -description


Prerequisite API to call to determine if the operation will be successful prior.


## -parameters




### -param keyCredentialManagerOperationType [in]

The intended operation from the <a href="security.keycredentialmanageroperationtype">KeyCredentialManagerOperationType</a>.


### -param isReady [out]

If the operational prerequisite will succeed (True) or (False).


### -param keyCredentialManagerOperationErrorStates [out]

Additional feedback about isReady represented by <a href="security.keycredentialmanageroperationerrorstates">KeyCredentialManagerOperationErrorStates</a>.


## -returns



Returns an HRESULT.



