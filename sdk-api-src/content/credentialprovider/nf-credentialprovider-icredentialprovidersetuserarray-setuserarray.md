---
UID: NF:credentialprovider.ICredentialProviderSetUserArray.SetUserArray
title: ICredentialProviderSetUserArray::SetUserArray (credentialprovider.h)
description: Called by the system during the initialization of a logon or credential UI to retrieve the set of users to show in that UI.
helpviewer_keywords: ["ICredentialProviderSetUserArray interface [Windows Shell]","SetUserArray method","ICredentialProviderSetUserArray.SetUserArray","ICredentialProviderSetUserArray::SetUserArray","SetUserArray","SetUserArray method [Windows Shell]","SetUserArray method [Windows Shell]","ICredentialProviderSetUserArray interface","credentialprovider/ICredentialProviderSetUserArray::SetUserArray","shell.ICredentialProviderSetUserArray_SetUserArray"]
old-location: shell\ICredentialProviderSetUserArray_SetUserArray.htm
tech.root: shell
ms.assetid: 14A9DFBD-7B44-4983-8B02-5880017B9B04
ms.date: 12/05/2018
ms.keywords: ICredentialProviderSetUserArray interface [Windows Shell],SetUserArray method, ICredentialProviderSetUserArray.SetUserArray, ICredentialProviderSetUserArray::SetUserArray, SetUserArray, SetUserArray method [Windows Shell], SetUserArray method [Windows Shell],ICredentialProviderSetUserArray interface, credentialprovider/ICredentialProviderSetUserArray::SetUserArray, shell.ICredentialProviderSetUserArray_SetUserArray
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderSetUserArray::SetUserArray
 - credentialprovider/ICredentialProviderSetUserArray::SetUserArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderSetUserArray.SetUserArray
---

# ICredentialProviderSetUserArray::SetUserArray


## -description

Called by the system during the initialization of a logon or credential UI to retrieve the set of users to show in that UI.

## -parameters

### -param users [in]

A pointer to an array object that contains a set of <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a> objects, each representing a user that will appear in the logon or credential UI. This array enables the credential provider to enumerate and query each of the user objects for their SID, their associated credential provider's ID, various forms of the user name, and their logon status string.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Note that this method does not transfer ownership of the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a> from the credential provider framework. The information it provides is cannot be altered.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidersetuserarray">ICredentialProviderSetUserArray</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a>