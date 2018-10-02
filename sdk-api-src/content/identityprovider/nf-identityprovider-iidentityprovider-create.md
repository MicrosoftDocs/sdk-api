---
UID: NF:identityprovider.IIdentityProvider.Create
title: IIdentityProvider::Create
author: windows-sdk-content
description: Creates a new identity associated with the specified user name.
old-location: security\iidentityprovider_create.htm
tech.root: secauthn
ms.assetid: 6ea1a87d-c8c1-43e4-b746-c1bfe98f370b
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Create, Create method [Security], Create method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],Create method, IIdentityProvider.Create, IIdentityProvider::Create, identityprovider/IIdentityProvider::Create, security.iidentityprovider_create
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
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
 - Identityprovider.h
api_name:
 - IIdentityProvider.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityProvider::Create


## -description


The <b>Create</b> method creates a new identity associated with the specified user name.


## -parameters




### -param lpszUserName [in]

The user name with which to associate the new identity.


### -param ppPropertyStore [out]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> interface that represents the property store associated with the new identity.


### -param pKeywordsToAdd [in, optional]

The properties to associate with the new identity.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

