---
UID: NF:credentialprovider.ICredentialProviderSetUserArray.SetUserArray
title: ICredentialProviderSetUserArray::SetUserArray
author: windows-sdk-content
description: Called by the system during the initialization of a logon or credential UI to retrieve the set of users to show in that UI.
old-location: shell\ICredentialProviderSetUserArray_SetUserArray.htm
tech.root: shell
ms.assetid: 14A9DFBD-7B44-4983-8B02-5880017B9B04
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICredentialProviderSetUserArray interface [Windows Shell],SetUserArray method, ICredentialProviderSetUserArray.SetUserArray, ICredentialProviderSetUserArray::SetUserArray, SetUserArray, SetUserArray method [Windows Shell], SetUserArray method [Windows Shell],ICredentialProviderSetUserArray interface, credentialprovider/ICredentialProviderSetUserArray::SetUserArray, shell.ICredentialProviderSetUserArray_SetUserArray
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
 - ICredentialProviderSetUserArray.SetUserArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- credentialprovider.h
: 
- ICredentialProviderSetUserArray.SetUserArray
: 
---

# ICredentialProviderSetUserArray::SetUserArray


## -description


Called by the system during the initialization of a logon or credential UI to retrieve the set of users to show in that UI.


## -parameters




### -param users [in]

A pointer to an array object that contains a set of <a href="https://msdn.microsoft.com/en-us/library/Hh706922(v=VS.85).aspx">ICredentialProviderUser</a> objects, each representing a user that will appear in the logon or credential UI. This array enables the credential provider to enumerate and query each of the user objects for their SID, their associated credential provider's ID, various forms of the user name, and their logon status string.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Note that this method does not transfer ownership of the <a href="https://msdn.microsoft.com/en-us/library/Hh706923(v=VS.85).aspx">ICredentialProviderUserArray</a> from the credential provider framework. The information it provides is cannot be altered.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh706920(v=VS.85).aspx">ICredentialProviderSetUserArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706922(v=VS.85).aspx">ICredentialProviderUser</a>
 

 

