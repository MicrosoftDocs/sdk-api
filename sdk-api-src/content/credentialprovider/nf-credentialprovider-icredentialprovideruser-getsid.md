---
UID: NF:credentialprovider.ICredentialProviderUser.GetSid
title: ICredentialProviderUser::GetSid
author: windows-sdk-content
description: Retrieves the user's security identifier (SID).
old-location: shell\ICredentialProviderUser_GetSid.htm
tech.root: shell
ms.assetid: FDC5D586-D72B-4eb1-BE7C-CFD8E0B48F48
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetSid, GetSid method [Windows Shell], GetSid method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetSid method, ICredentialProviderUser.GetSid, ICredentialProviderUser::GetSid, credentialprovider/ICredentialProviderUser::GetSid, shell.ICredentialProviderUser_GetSid
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
---

# ICredentialProviderUser::GetSid


## -description


Retrieves the user's security identifier (SID).


## -parameters




### -param sid [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the user's SID. It is the responsibility of the caller to free this resource by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This SID applies to both logon and credential UI.

This value can also be retrieved as a <b>PROPVARIANT</b> through <a href="https://msdn.microsoft.com/CA8CD897-127E-4113-A5A5-08110E0E6C17">ICredentialProviderUser::GetValue</a>.




## -see-also




<a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a>



<a href="https://msdn.microsoft.com/CA8CD897-127E-4113-A5A5-08110E0E6C17">ICredentialProviderUser::GetValue</a>
 

 

