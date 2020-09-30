---
UID: NF:bits10_3.IBackgroundCopyJobHttpOptions3.SetServerCertificateValidationInterface
title: IBackgroundCopyJobHttpOptions3::SetServerCertificateValidationInterface
ms.date: 05/09/2019
ms.keywords: IBackgroundCopyJobHttpOptions3::SetServerCertificateValidationInterface
description: Server certificates are sent when an HTTPS connection is opened. Use this method to set a callback to be called to validate those server certificates.
helpviewer_keywords: ["IBackgroundCopyJobHttpOptions3::SetServerCertificateValidationInterface"]
tech.root: Bits
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Bits.dll
req.header: bits10_3.h
req.idl: 
req.include-header: Bits.h
req.irql: 
req.kmdf-ver: 
req.lib: Bits.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - IBackgroundCopyJobHttpOptions3::SetServerCertificateValidationInterface
 - bits10_3/IBackgroundCopyJobHttpOptions3::SetServerCertificateValidationInterface
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - bits10_3.h
api_name:
 - IBackgroundCopyJobHttpOptions3::SetServerCertificateValidationInterface
---

## -description

Server certificates are sent when an HTTPS connection is opened. Use this method to set a callback to be called to validate those server certificates.

## -parameters

### -param certValidationCallback

Type: **[IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown)\***

A pointer to an object that implements [IBackgroundCopyServerCertificateValidationCallback](/windows/desktop/api/bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback). To remove the current callback interface pointer, set this parameter to `nullptr`.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_NOINTERFACE|You pass an interface pointer that cannot be queried for [IBackgroundCopyServerCertificateValidationCallback](/windows/desktop/api/bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback).|
|BG_E_READ_ONLY_WHEN_JOB_ACTIVE|The state of a job must be PAUSED to set the callback.|

## -remarks

Use this method when you want to perform your own checks on the server certificate.

Call this method only if you implement the [IBackgroundCopyServerCertificateValidationCallback](/windows/desktop/api/bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback) interface.

The validation interface becomes invalid when your application terminates; BITS does not maintain a record of the validation interface. As a result, your application's initialization process should call **SetServerCertificateValidationInterface** on those existing jobs for which you want to receive certificate validation requests.

If more than one application calls **SetServerCertificateValidationInterface** to set the notification interface for the job, the last application to call it is the one that will receive notifications. The other applications will not receive notifications.

If any certificate errors are found during the OS validation of the certificate, then the connection is aborted, and the custom callback is never called. You can customize the OS validation logic with a call to [IBackgroundCopyJobHttpOptions::SetSecurityFlags](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags). For example, you can ignore expected certificate validation errors.

If OS validation passes, then the [IBackgroundCopyServerCertificateValidationCallback::ValidateServerCertificate](./nf-bits10_3-ibackgroundcopyservercertificatevalidationcallback-validateservercertificate.md) method is called before completing the TLS handshake and before the HTTP request is sent.

If your validation method declines the certificate, the job will transition to **BG_JOB_STATE_TRANSIENT_ERROR** with a job error context of **BG_ERROR_CONTEXT_SERVER_CERTIFICATE_CALLBACK** and the error **HRESULT** from your callback. If your callback couldn't be called (for example, because BITS needed to validate a server certificate after your program exited), then the job error code will be **BG_E_SERVER_CERT_VALIDATION_INTERFACE_REQUIRED**. When your application is next run, it can fix this error by setting the validation callback again and resuming the job.

## -see-also

[IBackgroundCopyServerCertificateValidationCallback](/windows/desktop/api/bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)