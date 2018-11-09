---
UID: NF:credentialprovider.ICredentialProviderUserArray.GetAt
title: ICredentialProviderUserArray::GetAt
author: windows-sdk-content
description: Retrieves a specified user from the array.
old-location: shell\ICredentialProviderUserArray_GetAt.htm
tech.root: shell
ms.assetid: E768CC54-4392-4d5f-BB90-4AA91E5D8B00
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetAt, GetAt method [Windows Shell], GetAt method [Windows Shell],ICredentialProviderUserArray interface, ICredentialProviderUserArray interface [Windows Shell],GetAt method, ICredentialProviderUserArray.GetAt, ICredentialProviderUserArray::GetAt, credentialprovider/ICredentialProviderUserArray::GetAt, shell.ICredentialProviderUserArray_GetAt
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
 - ICredentialProviderUserArray.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderUserArray::GetAt


## -description


Retrieves a specified user from the array.


## -parameters




### -param userIndex [in]

The 0-based array index of the user. The size of the array can be obtained through the <a href="https://msdn.microsoft.com/en-us/library/Hh706926(v=VS.85).aspx">GetCount</a> method.


### -param user [out]

The address of a pointer to an object that, when this method returns successfully, represents the specified user. It is the responsibility of the caller to free this object when it is no longer needed by calling its <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> method.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The index specified in <i>userIndex</i> is out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh706923(v=VS.85).aspx">ICredentialProviderUserArray</a>
 

 

