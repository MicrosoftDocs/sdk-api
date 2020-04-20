---
UID: NF:credentialprovider.ICredentialProviderCredential.ReportResult
title: ICredentialProviderCredential::ReportResult (credentialprovider.h)
description: Translates a received error status code into the appropriate user-readable message.helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","ReportResult method","ICredentialProviderCredential.ReportResult","ICredentialProviderCredential::ReportResult","ReportResult","ReportResult method [Windows Shell]","ReportResult method [Windows Shell]","ICredentialProviderCredential interface","credentialprovider/ICredentialProviderCredential::ReportResult","shell.ICredentialProviderCredential_ReportResult","shell_ICredentialProviderCredential_ReportResult"]
old-location: shell\ICredentialProviderCredential_ReportResult.htm
tech.root: shell
ms.assetid: 13d6dda7-4a4f-45bf-af91-72f80497b9f7
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],ReportResult method, ICredentialProviderCredential.ReportResult, ICredentialProviderCredential::ReportResult, ReportResult, ReportResult method [Windows Shell], ReportResult method [Windows Shell],ICredentialProviderCredential interface, credentialprovider/ICredentialProviderCredential::ReportResult, shell.ICredentialProviderCredential_ReportResult, shell_ICredentialProviderCredential_ReportResult
f1_keywords:
- credentialprovider/ICredentialProviderCredential.ReportResult
dev_langs:
- c++
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
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
- COM
api_location:
- Credentialprovider.h
api_name:
- ICredentialProviderCredential.ReportResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredential::ReportResult


## -description


Translates a received error status code into the appropriate user-readable message. The Credential UI does not call this method.


## -parameters




### -param ntsStatus [in]

Type: <b>NTSTATUS</b>

The <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> value that reflects the return value of the <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/winlogon">Winlogon</a> call to <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.


### -param ntsSubstatus [in]

Type: <b>NTSTATUS</b>

The <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> value that reflects the value pointed to by the <i>SubStatus</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> when that function returns after being called by <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/winlogon">Winlogon</a>.


### -param ppszOptionalStatusText [out]

Type: <b>LPWSTR*</b>

A pointer to the error message that will be displayed to the user. May be <b>NULL</b>.


### -param pcpsiOptionalStatusIcon [out]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_status_icon">CREDENTIAL_PROVIDER_STATUS_ICON</a>*</b>

A pointer to an icon  that will shown on the credential. May be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required for Logon UI.

This method is used to report the outcome of a logon attempt back to a credential. The information in <i>ntsStatus</i> and <i>ntsSubstatus</i> can also be used when credential providers want to generate custom error messages. That status text from this call will be displayed on the selected credential.



