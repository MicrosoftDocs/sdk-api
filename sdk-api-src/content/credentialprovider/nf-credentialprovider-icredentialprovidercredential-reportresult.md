---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICredentialProviderCredential::ReportResult


## -description


Translates a received error status code into the appropriate user-readable message. The Credential UI does not call this method.


## -parameters




### -param ntsStatus [in]

Type: <b>NTSTATUS</b>

The <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> value that reflects the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> call to <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


### -param ntsSubstatus [in]

Type: <b>NTSTATUS</b>

The <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> value that reflects the value pointed to by the <i>SubStatus</i> parameter of <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> when that function returns after being called by <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a>.


### -param ppszOptionalStatusText [out]

Type: <b>LPWSTR*</b>

A pointer to the error message that will be displayed to the user. May be <b>NULL</b>.


### -param pcpsiOptionalStatusIcon [out]

Type: <b><a href="https://msdn.microsoft.com/2aa5b5dc-4756-4eff-a7d8-97c8a1dce41b">CREDENTIAL_PROVIDER_STATUS_ICON</a>*</b>

A pointer to an icon  that will shown on the credential. May be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required for Logon UI.

This method is used to report the outcome of a logon attempt back to a credential. The information in <i>ntsStatus</i> and <i>ntsSubstatus</i> can also be used when credential providers want to generate custom error messages. That status text from this call will be displayed on the selected credential.



