---
UID: NF:userconsentverifierinterop.IUserConsentVerifierInterop.RequestVerificationForWindowAsync
tech.root: winrt
title: IUserConsentVerifierInterop::RequestVerificationForWindowAsync
ms.date: 05/12/2021
targetos: Windows
description: Performs a verification using a device such as Microsoft Passport PIN, Windows Hello, or a fingerprint reader.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: userconsentverifierinterop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - userconsentverifierinterop.h
api_name:
 - IUserConsentVerifierInterop::RequestVerificationForWindowAsync
f1_keywords:
 - IUserConsentVerifierInterop::RequestVerificationForWindowAsync
 - userconsentverifierinterop/IUserConsentVerifierInterop::RequestVerificationForWindowAsync
dev_langs:
 - c++
---

## -description

Performs a verification using a device such as Microsoft Passport PIN, Windows Hello, or a fingerprint reader.

## -parameters

### -param appWindow

Handle to the window of the active application.

### -param message

A message to display to the user for this biometric verification request.

### -param riid

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example: 

`__uuidof(IAsyncOperation)` 

### -param asyncOperation

A [IAsyncOperation](/uwp/api/windows.foundation.iasyncoperation-1) value that returns a value from the [UserConsentVerificationResult](/uwp/api/windows.security.credentials.ui.userconsentverificationresult) enumeration.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

## -see-also

