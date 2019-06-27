---
UID: NF:credentialprovider.ICredentialProviderUser.GetSid
title: ICredentialProviderUser::GetSid (credentialprovider.h)
author: windows-sdk-content
description: Retrieves the user's security identifier (SID).
old-location: shell\ICredentialProviderUser_GetSid.htm
tech.root: shell
ms.assetid: FDC5D586-D72B-4eb1-BE7C-CFD8E0B48F48
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSid, GetSid method [Windows Shell], GetSid method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetSid method, ICredentialProviderUser.GetSid, ICredentialProviderUser::GetSid, credentialprovider/ICredentialProviderUser::GetSid, shell.ICredentialProviderUser_GetSid
ms.topic: method
f1_keywords: 
 - "credentialprovider/ICredentialProviderUser.GetSid"
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUser.GetSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderUser::GetSid


## -description


Retrieves the user's security identifier (SID).


## -parameters




### -param sid [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the user's SID. It is the responsibility of the caller to free this resource by calling the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This SID applies to both logon and credential UI.

This value can also be retrieved as a <b>PROPVARIANT</b> through <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">ICredentialProviderUser::GetValue</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">ICredentialProviderUser::GetValue</a>
 

 

