---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.EndFieldUpdates
title: ICredentialProviderCredentialEvents2::EndFieldUpdates (credentialprovider.h)
author: windows-sdk-content
description: Finishes and commits the batch updates started by BeginFieldUpdates.
old-location: shell\ICredentialProviderCredentialEvents2_EndFieldUpdates.htm
tech.root: shell
ms.assetid: D05A558E-79D9-4063-A714-F54D8EB8BBF8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndFieldUpdates, EndFieldUpdates method [Windows Shell], EndFieldUpdates method [Windows Shell],ICredentialProviderCredentialEvents2 interface, ICredentialProviderCredentialEvents2 interface [Windows Shell],EndFieldUpdates method, ICredentialProviderCredentialEvents2.EndFieldUpdates, ICredentialProviderCredentialEvents2::EndFieldUpdates, credentialprovider/ICredentialProviderCredentialEvents2::EndFieldUpdates, shell.ICredentialProviderCredentialEvents2_EndFieldUpdates
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialEvents2.EndFieldUpdates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents2::EndFieldUpdates


## -description


Finishes and commits the batch updates started by <a href="https://msdn.microsoft.com/2E7EB8B4-ED6F-4954-88D3-FB79D80E53B2">BeginFieldUpdates</a>.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A call to this method must be made at the end of the code that updates the credential's UI fields.




## -see-also




<a href="https://msdn.microsoft.com/2E7EB8B4-ED6F-4954-88D3-FB79D80E53B2">ICredentialProviderCredential2::BeginFieldUpdates</a>



<a href="https://msdn.microsoft.com/5507E8DE-5746-4031-900B-3EF5C97BC2EE">ICredentialProviderCredential2::SetFieldOptions</a>



<a href="https://msdn.microsoft.com/47290FF7-1785-4470-B3A9-F35C5028A6FE">ICredentialProviderCredentialEvents2</a>
 

 

