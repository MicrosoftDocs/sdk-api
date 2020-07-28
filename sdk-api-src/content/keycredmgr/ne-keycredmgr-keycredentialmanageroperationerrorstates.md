---
UID: NE:keycredmgr.KeyCredentialManagerOperationErrorStates
title: KeyCredentialManagerOperationErrorStates (keycredmgr.h)
description: Enumeration of Error states returned by the function KeyCredentialManagerGetOperationErrorStates as flags.
helpviewer_keywords: ["KeyCredentialManagerOperationErrorStateCertificateFailure","KeyCredentialManagerOperationErrorStateDeviceJoinFailure","KeyCredentialManagerOperationErrorStateHardwareFailure","KeyCredentialManagerOperationErrorStateNone","KeyCredentialManagerOperationErrorStatePinExistsFailure","KeyCredentialManagerOperationErrorStatePolicyFailure","KeyCredentialManagerOperationErrorStateRemoteSessionFailure","KeyCredentialManagerOperationErrorStateTokenFailure","KeyCredentialManagerOperationErrorStates","KeyCredentialManagerOperationErrorStates enumeration [Security]","keycredmgr/KeyCredentialManagerOperationErrorStateCertificateFailure","keycredmgr/KeyCredentialManagerOperationErrorStateDeviceJoinFailure","keycredmgr/KeyCredentialManagerOperationErrorStateHardwareFailure","keycredmgr/KeyCredentialManagerOperationErrorStateNone","keycredmgr/KeyCredentialManagerOperationErrorStatePinExistsFailure","keycredmgr/KeyCredentialManagerOperationErrorStatePolicyFailure","keycredmgr/KeyCredentialManagerOperationErrorStateRemoteSessionFailure","keycredmgr/KeyCredentialManagerOperationErrorStateTokenFailure","keycredmgr/KeyCredentialManagerOperationErrorStates","security.keycredentialmanageroperationerrorstates"]
old-location: security\keycredentialmanageroperationerrorstates.htm
tech.root: security
ms.assetid: 51C460E3-0A74-40A8-9F41-057EF6D03E86
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerOperationErrorStateCertificateFailure, KeyCredentialManagerOperationErrorStateDeviceJoinFailure, KeyCredentialManagerOperationErrorStateHardwareFailure, KeyCredentialManagerOperationErrorStateNone, KeyCredentialManagerOperationErrorStatePinExistsFailure, KeyCredentialManagerOperationErrorStatePolicyFailure, KeyCredentialManagerOperationErrorStateRemoteSessionFailure, KeyCredentialManagerOperationErrorStateTokenFailure, KeyCredentialManagerOperationErrorStates, KeyCredentialManagerOperationErrorStates enumeration [Security], keycredmgr/KeyCredentialManagerOperationErrorStateCertificateFailure, keycredmgr/KeyCredentialManagerOperationErrorStateDeviceJoinFailure, keycredmgr/KeyCredentialManagerOperationErrorStateHardwareFailure, keycredmgr/KeyCredentialManagerOperationErrorStateNone, keycredmgr/KeyCredentialManagerOperationErrorStatePinExistsFailure, keycredmgr/KeyCredentialManagerOperationErrorStatePolicyFailure, keycredmgr/KeyCredentialManagerOperationErrorStateRemoteSessionFailure, keycredmgr/KeyCredentialManagerOperationErrorStateTokenFailure, keycredmgr/KeyCredentialManagerOperationErrorStates, security.keycredentialmanageroperationerrorstates
f1_keywords:
- keycredmgr/KeyCredentialManagerOperationErrorStates
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- keycredmgr.h
api_name:
- KeyCredentialManagerOperationErrorStates
targetos: Windows
req.typenames: KeyCredentialManagerOperationErrorStates
req.redist: 
ms.custom: 19H1
---

# KeyCredentialManagerOperationErrorStates enumeration


## -description


Enumeration of Error states returned by the function <a href="https://msdn.microsoft.com/en-us/library/Mt830288(v=VS.85).aspx">KeyCredentialManagerGetOperationErrorStates</a> as flags.


## -enum-fields




### -field KeyCredentialManagerOperationErrorStateNone

No Error  equivalent to ERROR_SUCCESS.


### -field KeyCredentialManagerOperationErrorStateDeviceJoinFailure

WHFB enrollment will successfully complete because the device is not properly joined to Azure or the Enterprise.


### -field KeyCredentialManagerOperationErrorStateTokenFailure

WHFB enrollment will not successfully complete because the user could not get a token from Azure or the Enterprise.


### -field KeyCredentialManagerOperationErrorStateCertificateFailure

WHFB enrollment will not successfully complete because the certificate authority and/or certificate template could not be found.


### -field KeyCredentialManagerOperationErrorStateRemoteSessionFailure

WHFB enrollment will not successfully complete because the current session is a remote session. 


### -field KeyCredentialManagerOperationErrorStatePolicyFailure

WHFB enrollment will not successfully complete because there was an error reading MDM or Group Policy. 


### -field KeyCredentialManagerOperationErrorStateHardwareFailure

WHFB enrollment will not successful complete because the device does not have the required hardware.


### -field KeyCredentialManagerOperationErrorStatePinExistsFailure

WHFB is already enrolled on this device. 

