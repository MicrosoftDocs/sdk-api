---
UID: NF:credentialprovider.ICredentialProviderUser.GetProviderID
title: ICredentialProviderUser::GetProviderID method
author: windows-driver-content
description: Retrieves the ID of the account provider for this user.
old-location: shell\ICredentialProviderUser_GetProviderID.htm
old-project: shell
ms.assetid: 7BD6C532-0266-4579-96FA-91D0AF7E6C4C
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetProviderID method [Windows Shell], GetProviderID method [Windows Shell], ICredentialProviderUser interface, GetProviderID,ICredentialProviderUser.GetProviderID, ICredentialProviderUser, ICredentialProviderUser interface [Windows Shell], GetProviderID method, ICredentialProviderUser::GetProviderID, credentialprovider/ICredentialProviderUser::GetProviderID, shell.ICredentialProviderUser_GetProviderID
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
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Authui.dll
api_name:
-	ICredentialProviderUser.GetProviderID
product: Windows
targetos: Windows
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
---

# ICredentialProviderUser::GetProviderID method


## -description


Retrieves the ID of the account provider for this user.


## -parameters




### -param providerID [out]

A pointer to a value that, when this method returns successfully, receives the GUID of the user's account provider.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This GUID applies to both logon and credential UI.

This value can also be retrieved as a <b>PROPVARIANT</b> through <a href="https://msdn.microsoft.com/CA8CD897-127E-4113-A5A5-08110E0E6C17">ICredentialProviderUser::GetValue</a>.




## -see-also




<a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a>



<a href="https://msdn.microsoft.com/CA8CD897-127E-4113-A5A5-08110E0E6C17">ICredentialProviderUser::GetValue</a>
 

 

