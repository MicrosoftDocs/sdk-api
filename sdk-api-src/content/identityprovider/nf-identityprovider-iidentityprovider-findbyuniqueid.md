---
UID: NF:identityprovider.IIdentityProvider.FindByUniqueID
title: IIdentityProvider::FindByUniqueID
author: windows-sdk-content
description: Retrieves a pointer to the IPropertyStore interface instance associated with the specified identity.
old-location: security\iidentityprovider_findbyuniqueid.htm
old-project: SecAuthN
ms.assetid: 26a0e247-0387-4455-9510-bd0e6adc0213
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: FindByUniqueID, FindByUniqueID method [Security], FindByUniqueID method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],FindByUniqueID method, IIdentityProvider.FindByUniqueID, IIdentityProvider::FindByUniqueID, identityprovider/IIdentityProvider::FindByUniqueID, security.iidentityprovider_findbyuniqueid
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: IDENTITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Identityprovider.h
api_name:
-	IIdentityProvider.FindByUniqueID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityProvider::FindByUniqueID


## -description


The <b>FindByUniqueID</b> method retrieves a pointer to the <b>IPropertyStore</b> interface instance associated with the specified identity.


## -parameters




### -param lpszUniqueID [in]

The unique identity to find.


### -param ppPropertyStore [out]

A pointer to the instance of the <b>IPropertyStore</b> interface associated with the specified identity.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

