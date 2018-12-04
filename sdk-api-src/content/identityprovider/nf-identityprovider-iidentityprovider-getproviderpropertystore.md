---
UID: NF:identityprovider.IIdentityProvider.GetProviderPropertyStore
title: IIdentityProvider::GetProviderPropertyStore
author: windows-sdk-content
description: Retrieves a pointer to the IPropertyStore interface associated with the identity provider.
old-location: security\iidentityprovider_getproviderpropertystore.htm
tech.root: secauthn
ms.assetid: e0a8f732-5675-49f7-8c2f-6e5f8f1be957
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetProviderPropertyStore, GetProviderPropertyStore method [Security], GetProviderPropertyStore method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],GetProviderPropertyStore method, IIdentityProvider.GetProviderPropertyStore, IIdentityProvider::GetProviderPropertyStore, identityprovider/IIdentityProvider::GetProviderPropertyStore, security.iidentityprovider_getproviderpropertystore
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
 - IIdentityProvider.GetProviderPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityProvider::GetProviderPropertyStore


## -description


The <b>GetProviderPropertyStore</b> method retrieves a pointer to the <b>IPropertyStore</b> interface associated with the identity provider.


## -parameters




### -param ppPropertyStore [out]

A pointer to the global <b>IPropertyStore</b> interface associated with this identity provider.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

