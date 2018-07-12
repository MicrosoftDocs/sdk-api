---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.BeginFieldUpdates
title: ICredentialProviderCredentialEvents2::BeginFieldUpdates
author: windows-sdk-content
description: Starts a batch update to fields in the logon or credential UI.
old-location: shell\ICredentialProviderCredentialEvents2_BeginFieldUpdates.htm
old-project: shell
ms.assetid: 2E7EB8B4-ED6F-4954-88D3-FB79D80E53B2
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: BeginFieldUpdates, BeginFieldUpdates method [Windows Shell], BeginFieldUpdates method [Windows Shell],ICredentialProviderCredentialEvents2 interface, ICredentialProviderCredentialEvents2 interface [Windows Shell],BeginFieldUpdates method, ICredentialProviderCredentialEvents2.BeginFieldUpdates, ICredentialProviderCredentialEvents2::BeginFieldUpdates, credentialprovider/ICredentialProviderCredentialEvents2::BeginFieldUpdates, shell.ICredentialProviderCredentialEvents2_BeginFieldUpdates
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialEvents2.BeginFieldUpdates
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredentialEvents2::BeginFieldUpdates


## -description


Starts a batch update to fields in the logon or credential UI.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A call to this method must be made at the beginning of the code that updates the credential's UI fields.




## -see-also




<a href="https://msdn.microsoft.com/C1C4BF88-3151-4a8b-A1EE-9616DCB6EA58">ICredentialProviderCredential2</a>



<a href="https://msdn.microsoft.com/D05A558E-79D9-4063-A714-F54D8EB8BBF8">ICredentialProviderCredential2::EndFieldUpdates</a>



<a href="https://msdn.microsoft.com/5507E8DE-5746-4031-900B-3EF5C97BC2EE">ICredentialProviderCredential2::SetFieldOptions</a>



<a href="https://msdn.microsoft.com/47290FF7-1785-4470-B3A9-F35C5028A6FE">ICredentialProviderCredentialEvents2</a>
 

 

