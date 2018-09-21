---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.BeginFieldUpdates
title: ICredentialProviderCredentialEvents2::BeginFieldUpdates
author: windows-sdk-content
description: Starts a batch update to fields in the logon or credential UI.
old-location: shell\ICredentialProviderCredentialEvents2_BeginFieldUpdates.htm
tech.root: shell
ms.assetid: 2E7EB8B4-ED6F-4954-88D3-FB79D80E53B2
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: BeginFieldUpdates, BeginFieldUpdates method [Windows Shell], BeginFieldUpdates method [Windows Shell],ICredentialProviderCredentialEvents2 interface, ICredentialProviderCredentialEvents2 interface [Windows Shell],BeginFieldUpdates method, ICredentialProviderCredentialEvents2.BeginFieldUpdates, ICredentialProviderCredentialEvents2::BeginFieldUpdates, credentialprovider/ICredentialProviderCredentialEvents2::BeginFieldUpdates, shell.ICredentialProviderCredentialEvents2_BeginFieldUpdates
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICredentialProviderCredentialEvents2.BeginFieldUpdates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Hh706912(v=VS.85).aspx">ICredentialProviderCredential2</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706916(v=VS.85).aspx">ICredentialProviderCredential2::EndFieldUpdates</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706917(v=VS.85).aspx">ICredentialProviderCredential2::SetFieldOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706914(v=VS.85).aspx">ICredentialProviderCredentialEvents2</a>
 

 

