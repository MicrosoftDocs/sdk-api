---
UID: NF:credentialprovider.ICredentialProviderFilter.UpdateRemoteCredential
title: ICredentialProviderFilter::UpdateRemoteCredential
author: windows-sdk-content
description: Updates a credential from a remote session.
old-location: shell\ICredentialProviderFilter_UpdateRemoteCredential.htm
tech.root: shell
ms.assetid: d0730f67-e4f1-42b2-823a-75b08a5c952e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICredentialProviderFilter interface [Windows Shell],UpdateRemoteCredential method, ICredentialProviderFilter.UpdateRemoteCredential, ICredentialProviderFilter::UpdateRemoteCredential, UpdateRemoteCredential, UpdateRemoteCredential method [Windows Shell], UpdateRemoteCredential method [Windows Shell],ICredentialProviderFilter interface, _shell_ICredentialProviderFilter_UpdateRemoteCredential, credentialprovider/ICredentialProviderFilter::UpdateRemoteCredential, shell.ICredentialProviderFilter_UpdateRemoteCredential
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICredentialProviderFilter.UpdateRemoteCredential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderFilter::UpdateRemoteCredential


## -description


Updates a credential from a remote session.


## -parameters




### -param pcpcsIn [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A constant pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure.


### -param pcpcsOut [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



